# PSS スクラッチ組織設定ガイド

## スクラッチ組織定義ファイルの設定内容

このプロジェクトの `config/project-scratch-def.json` には、PSS カスタマーポータル環境に必要な以下の機能が設定されています。

### 有効化された機能 (Features)

#### 必須機能

1. **ServiceCloud**
   - Service Cloud の全機能を有効化
   - ケース管理、オムニチャネル、サービスコンソールが利用可能

2. **OmniStudioRuntime**
   - OmniStudio のランタイム機能
   - FlexCards、OmniScripts の実行環境

3. **OmniStudioDesigner**
   - OmniStudio のデザイナー機能
   - ローコード開発ツールへのアクセス

4. **MultiCurrency**
   - 複数通貨対応
   - 国際的な助成金管理に対応

5. **EnableSetPasswordInApi**
   - API 経由でのパスワード設定
   - テストデータ作成の自動化に必要

### 有効化された設定 (Settings)

#### Experience Cloud (Communities)
```json
"communitiesSettings": {
  "enableNetworksEnabled": true
}
```
- 市民向けカスタマーポータルの構築に必須

#### Knowledge
```json
"knowledgeSettings": {
  "enableKnowledge": true,
  "enableCreateEditOnArticlesTab": true,
  "enableExternalMediaContent": true
}
```
- ナレッジベース、FAQ、セルフサービス機能

#### Person Accounts
```json
"accountSettings": {
  "enablePersonAccounts": true
}
```
- 市民の個人情報を Account オブジェクトで管理
- B2C シナリオに最適

#### Case Management
```json
"caseSettings": {
  "emailToCase": true,
  "webToCase": true
}
```
- メールからケース作成
- Web フォームからケース作成

#### Omni-Channel
```json
"omniChannelSettings": {
  "enableOmniChannel": true
}
```
- ケースの自動割り当て
- エージェントの作業管理

#### その他の機能
- **Enhanced Notes**: 拡張メモ機能
- **Path Assistant**: プロセスガイダンス
- **Chatter**: 内部コラボレーション
- **Lightning Experience**: モダンな UI

## スクラッチ組織の作成方法

### 1. Dev Hub への認証

```bash
sf org login web --set-default-dev-hub --alias DevHub
```

### 2. スクラッチ組織の作成

```bash
sf org create scratch --definition-file config/project-scratch-def.json --alias pss-scratch --set-default --duration-days 30
```

パラメータ:
- `--definition-file`: スクラッチ組織定義ファイルのパス
- `--alias`: スクラッチ組織のエイリアス名
- `--set-default`: デフォルトの組織として設定
- `--duration-days`: 有効期間 (最大 30 日)

### 3. スクラッチ組織を開く

```bash
sf org open --target-org pss-scratch
```

### 4. 組織の確認

```bash
# 組織の一覧表示
sf org list

# 組織の詳細表示
sf org display --target-org pss-scratch
```

## 注意事項

### Person Accounts について

Person Accounts を有効化すると、以下の点に注意が必要です:

1. **有効化後は無効化できない**: 一度有効化すると元に戻せません
2. **Account と Contact の関係が変わる**: 個人アカウントでは Account と Contact が 1:1 の関係になります
3. **レコードタイプが必要**: Business Account と Person Account を区別するためのレコードタイプが自動作成されます

### OmniStudio について

OmniStudio を使用する際の注意点:

1. **ライセンス**: スクラッチ組織では自動的にライセンスが付与されます
2. **メタデータ形式**: OmniStudio のメタデータは特殊な形式です
3. **デプロイ**: 本番環境へのデプロイ時は OmniStudio のライセンスが必要です

### Experience Cloud について

Experience Cloud を使用する際の手順:

1. スクラッチ組織作成後、Setup > Digital Experiences > All Sites から新規サイトを作成
2. テンプレートを選択 (Customer Service など)
3. サイトの URL とドメインを設定
4. ゲストユーザープロファイルとメンバープロファイルを設定

## トラブルシューティング

### エラー: "This feature isn't enabled for your org"

**原因**: 機能名が正しくないか、その機能がスクラッチ組織でサポートされていない

**解決策**:
1. 機能名のスペルを確認
2. Salesforce のドキュメントで機能の可用性を確認
3. 不要な機能を削除して再試行

### エラー: "Person accounts can't be enabled in a scratch org"

**原因**: 一部の環境では Person Accounts がサポートされていない

**解決策**:
1. `accountSettings.enablePersonAccounts` を `false` に変更
2. または、この設定を削除

### スクラッチ組織の作成が遅い

**原因**: 多くの機能を有効化すると作成に時間がかかる

**対策**:
- 初期開発では最小限の機能のみ有効化
- 必要に応じて後から機能を追加

## 参考リンク

- [Salesforce DX Developer Guide - Scratch Org Definition](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file.htm)
- [Scratch Org Features](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm)
- [OmniStudio Documentation](https://help.salesforce.com/s/articleView?id=sf.os_overview.htm)
- [Experience Cloud Documentation](https://help.salesforce.com/s/articleView?id=sf.networks_overview.htm)

---

**作成日**: 2026-01-09  
**最終更新日**: 2026-01-09
