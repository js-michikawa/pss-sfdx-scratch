# スクラッチ組織の検証とコミットワークフロー

## 概要

スクラッチ組織の設定を変更した後、本番環境やチームメンバーに影響を与えないよう、必ず以下のワークフローに従ってください。

## ワークフロー

### 1. 設定の変更

Setup で必要な設定を有効化します。

**例**:
- OmniStudio 設定の有効化
- Timeline の有効化
- その他の機能設定

### 2. メタデータの取得

設定を変更したら、メタデータを取得します。

```bash
# 全ての設定メタデータを取得
sf project retrieve start --metadata Settings --wait 30
```

### 3. 不要なメタデータの削除

⚠️ **重要**: `sf project retrieve start --metadata Settings` を実行すると、139個もの設定ファイルが取得されます。**必ずプロジェクトに必要なファイルのみを残してください。**

#### 3-1. 取得されたファイルを確認

```bash
# 取得されたファイル数を確認
Get-ChildItem -Path "force-app\main\default\settings" | Measure-Object

# ファイル一覧を表示
Get-ChildItem -Path "force-app\main\default\settings" | Select-Object Name
```

#### 3-2. 必要なファイルを特定

**PSS プロジェクトで必要な設定ファイル**:
- `OmniStudio.settings-meta.xml` - OmniStudio の設定 (手動で ON にした設定)

**不要な設定ファイルの例**:
- `Communities.settings-meta.xml` - `project-scratch-def.json` の `settings` で管理
- `Knowledge.settings-meta.xml` - `project-scratch-def.json` の `settings` で管理
- `Case.settings-meta.xml` - `project-scratch-def.json` の `settings` で管理
- その他の Industry Cloud 関連ファイル (Analytics, HealthCloud, FinancialServices など)

**判断基準**:
1. `project-scratch-def.json` の `settings` セクションで既に定義されている設定 → **不要**
2. `project-scratch-def.json` の `features` で有効化されている機能 → **不要**
3. Setup で手動で ON にした設定で、メタデータとして管理したいもの → **必要**

#### 3-3. 不要なファイルを削除

**方法1: 必要なファイルのみを残して削除**

```powershell
# 必要なファイルのリストを定義
$keepFiles = @(
    "OmniStudio.settings-meta.xml"
)

# 必要なファイル以外を削除
Get-ChildItem -Path "force-app\main\default\settings" | 
    Where-Object { $_.Name -notin $keepFiles } | 
    Remove-Item -Force
```

**方法2: 不要なディレクトリも削除**

```powershell
# settings 以外のディレクトリを削除
Get-ChildItem -Path "force-app\main\default" -Directory | 
    Where-Object { $_.Name -ne "settings" } | 
    Remove-Item -Recurse -Force
```

#### 3-4. 削除結果を確認

```bash
# 残ったファイルを確認
Get-ChildItem -Path "force-app\main\default\settings"

# Git の変更状況を確認
git status --short
```

### 4. スクラッチ組織の削除と再作成

メタデータが正しく機能するか検証するため、スクラッチ組織を削除して再作成します。

```bash
# 現在のスクラッチ組織を削除
sf org delete scratch --target-org pss-scratch --no-prompt

# 新しいスクラッチ組織を作成 (--wait 30 を必ず指定)
sf org create scratch --definition-file config/project-scratch-def.json --alias pss-scratch --set-default --duration-days 30 --wait 30
```

### 5. 検証

スクラッチ組織を開いて、設定が正しく反映されているか確認します。

```bash
# スクラッチ組織を開く
sf org open
```

**確認項目**:
- Setup で設定した機能が有効化されているか
- エラーが発生していないか
- 必要なオブジェクトやコンポーネントが利用可能か

### 6. コミット前の確認 ✅

**⚠️ 必須**: コミット前に必ず以下を確認してください。

#### チェックリスト

```bash
# 1. 変更されたファイルを確認
git status

# 2. 各ファイルの差分を確認
git diff

# 3. force-app ディレクトリの内容を確認
git ls-files force-app/
```

**確認項目**:

- [ ] **不要な設定ファイルが含まれていないか**
  - `force-app/main/default/settings/` に必要なファイルのみが存在するか
  - Industry Cloud 関連の不要なファイル (Analytics, HealthCloud など) が含まれていないか
  
- [ ] **不要なディレクトリが含まれていないか**
  - `force-app/main/default/` に `settings` 以外のディレクトリがないか
  - `applications`, `aura`, `classes`, `objects` などが含まれていないか

- [ ] **project-scratch-def.json の変更が意図したものか**
  - 不要な feature が追加されていないか
  - JSON フォーマットが正しいか

- [ ] **ドキュメントの内容が正しいか**
  - 追加したドキュメントに誤りがないか
  - リンクが正しく機能するか

#### 問題が見つかった場合

```bash
# ステージングから削除
git reset HEAD <ファイル名>

# ファイルを削除
Remove-Item -Path "<ファイルパス>" -Force

# 再度確認
git status
```

### 7. コミット

検証が成功し、確認チェックリストを全てクリアしたら、変更をコミットします。

```bash
# 変更をステージング
git add .

# コミット (わかりやすいメッセージを記載)
git commit -m "Add OmniStudio and Timeline settings metadata"

# リモートにプッシュ
git push
```

## 重要な注意事項

### ⚠️ 必ず検証してからコミット

- **検証なしでコミットしない**: 設定ミスや不要なメタデータが混入すると、チームメンバーのスクラッチ組織作成時にエラーが発生します
- **Industry Cloud メタデータに注意**: 不要な Industry Cloud 関連のメタデータが混入しないよう、必要なファイルのみを残してください

### ✅ タイムアウトオプションの必須化

スクラッチ組織の作成とメタデータのデプロイには、必ず `--wait 30` オプションを指定してください。

**理由**:
- デフォルトのタイムアウト (6分) では、大規模な設定やメタデータのデプロイが完了しない場合があります
- 30分のタイムアウトを設定することで、確実に完了を待つことができます

**コマンド例**:
```bash
# スクラッチ組織作成
sf org create scratch --definition-file config/project-scratch-def.json --alias pss-scratch --set-default --duration-days 30 --wait 30

# メタデータデプロイ
sf project deploy start --wait 30

# メタデータ取得
sf project retrieve start --metadata Settings --wait 30
```

## トラブルシューティング

### スクラッチ組織の作成に失敗する

**原因**:
- `project-scratch-def.json` に無効な feature が含まれている
- JSON のフォーマットエラー (余分な空行、カンマなど)

**対処法**:
1. `project-scratch-def.json` の構文を確認
2. 無効な feature を削除
3. JSON フォーマットを確認

### メタデータのデプロイでエラーが発生する

**原因**:
- 不要な Industry Cloud メタデータが混入している
- 設定ファイルの内容が現在の組織と互換性がない

**対処法**:
1. 必要な設定ファイルのみを残す
2. 設定ファイルの内容を確認し、不要な設定を削除

## ベストプラクティス

1. **小さな変更を頻繁にコミット**: 大きな変更をまとめてコミットせず、小さな変更を頻繁にコミットすることで、問題の特定が容易になります

2. **コミットメッセージを明確に**: 何を変更したか、なぜ変更したかを明確に記載します

3. **チームに通知**: 重要な設定変更を行った場合は、チームメンバーに通知します

4. **ドキュメントを更新**: 新しい設定を追加した場合は、README やナレッジベースを更新します

## まとめ

このワークフローに従うことで、スクラッチ組織の設定変更を安全に管理し、チーム全体で一貫した開発環境を維持できます。
