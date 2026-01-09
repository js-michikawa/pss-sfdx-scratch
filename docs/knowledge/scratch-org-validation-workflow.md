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

取得したメタデータから、プロジェクトに必要なファイルのみを残します。

**必要な設定ファイルの例** (PSS プロジェクト):
- `OmniStudio.settings-meta.xml`
- `Communities.settings-meta.xml`
- `Knowledge.settings-meta.xml`
- `PathAssistant.settings-meta.xml`
- `Chatter.settings-meta.xml`
- `Case.settings-meta.xml`
- `OmniChannel.settings-meta.xml`

**PowerShell で不要なファイルを削除**:
```powershell
# 必要なファイルのみを残して削除
Remove-Item -Path "force-app\main\default\settings\*" `
  -Exclude "OmniStudio.settings-meta.xml","Communities.settings-meta.xml","Knowledge.settings-meta.xml","PathAssistant.settings-meta.xml","Chatter.settings-meta.xml","Case.settings-meta.xml","OmniChannel.settings-meta.xml" `
  -Force

# 不要なディレクトリを削除
Remove-Item -Path "force-app\main\default\*" -Exclude "settings" -Recurse -Force
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

### 6. コミット

検証が成功したら、変更をコミットします。

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
