---
description: メタデータ取得後の精査とコミット前の確認
---

# メタデータ取得後の精査とコミットワークフロー

このワークフローは、Setup で設定を変更した後、メタデータを取得してコミットするまでの手順を定義します。

## 前提条件

- Setup で必要な設定を有効化済み
- スクラッチ組織が作成済み

## ステップ

### 1. メタデータを取得

```bash
sf project retrieve start --metadata Settings --wait 30
```

### 2. 取得されたファイル数を確認

```powershell
Get-ChildItem -Path "force-app\main\default\settings" | Measure-Object
```

**期待値**: 139個のファイルが取得される

### 3. 必要なファイルのみを残して削除

```powershell
# 必要なファイルのリストを定義
$keepFiles = @(
    "OmniStudio.settings-meta.xml"
)

# 必要なファイル以外を削除
Get-ChildItem -Path "force-app\main\default\settings" | 
    Where-Object { $_.Name -notin $keepFiles } | 
    Remove-Item -Force

# settings 以外のディレクトリを削除
Get-ChildItem -Path "force-app\main\default" -Directory | 
    Where-Object { $_.Name -ne "settings" } | 
    Remove-Item -Recurse -Force
```

### 4. 削除結果を確認

```powershell
# 残ったファイルを確認
Get-ChildItem -Path "force-app\main\default\settings"

# Git の変更状況を確認
git status --short
```

**期待値**: 必要なファイルのみが残っている

### 5. コミット前の確認チェックリスト

```bash
# 変更されたファイルを確認
git status

# 各ファイルの差分を確認
git diff

# force-app ディレクトリの内容を確認
git ls-files force-app/
```

**確認項目**:
- [ ] 不要な設定ファイルが含まれていないか
- [ ] 不要なディレクトリが含まれていないか
- [ ] project-scratch-def.json の変更が意図したものか
- [ ] ドキュメントの内容が正しいか

### 6. スクラッチ組織を削除して再作成

```bash
# 現在のスクラッチ組織を削除
sf org delete scratch --target-org pss-scratch --no-prompt

# 新しいスクラッチ組織を作成
sf org create scratch --definition-file config/project-scratch-def.json --alias pss-scratch --set-default --duration-days 30 --wait 30
```

### 7. メタデータをデプロイ

```bash
sf project deploy start --source-dir force-app/main/default/settings --wait 30
```

### 8. 設定が反映されているか確認

```bash
# OmniStudio Settings ページを開く
sf org open --path "/lightning/setup/OmniStudioSettings/home"
```

ブラウザで設定が正しく反映されているか確認する

### 9. コミット

全ての確認が完了したら、変更をコミット

```bash
git add .
git commit -m "Add OmniStudio settings metadata"
git push
```

## 注意事項

- メタデータ取得後は必ず不要なファイルを削除する
- コミット前に必ずチェックリストを確認する
- スクラッチ組織の作成回数には制限があるため、慎重に実行する
