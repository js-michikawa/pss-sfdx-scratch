# Salesforce DX (SFDX) 基礎ナレッジ

## SFDX とは

Salesforce DX は、Salesforce プラットフォーム上でのモダンな開発体験を提供するツールセットです。ソース駆動型の開発、チーム開発、継続的インテグレーション/継続的デリバリー (CI/CD) をサポートします。

## 主要な概念

### 1. スクラッチ組織 (Scratch Org)

- **定義**: 一時的な Salesforce 環境で、開発とテストに使用
- **特徴**:
  - 最大 30 日間利用可能
  - コードで定義可能 (Infrastructure as Code)
  - 複数の開発者が独立した環境で作業可能
  - 本番環境に影響を与えずにテスト可能

### 2. Dev Hub

- **定義**: スクラッチ組織を作成・管理するための中央管理組織
- **要件**: Production または Developer Edition 組織で有効化が必要
- **機能**:
  - スクラッチ組織の作成と管理
  - 使用状況の監視
  - ライセンス管理

### 3. ソース形式

- **メタデータ API 形式**: 従来の形式 (XML ベース)
- **ソース形式**: SFDX 推奨の形式
  - より細かい粒度
  - Git フレンドリー
  - マージコンフリクトの削減

## Salesforce CLI の主要コマンド

### 組織管理

```bash
# Dev Hub への認証
sf org login web --set-default-dev-hub --alias DevHub

# スクラッチ組織の作成
sf org create scratch --definition-file config/project-scratch-def.json --alias MyScratchOrg --set-default

# 組織を開く
sf org open

# 組織の一覧表示
sf org list

# 組織の削除
sf org delete scratch --target-org MyScratchOrg
```

### プロジェクト管理

```bash
# 新規プロジェクトの作成
sf project generate --name MyProject

# メタデータのデプロイ (プッシュ)
sf project deploy start

# メタデータの取得 (プル)
sf project retrieve start

# 特定のメタデータの取得
sf project retrieve start --metadata ApexClass:MyClass
```

### データ管理

```bash
# データのエクスポート
sf data export tree --query "SELECT Id, Name FROM Account" --output-dir ./data

# データのインポート
sf data import tree --plan ./data/Account-plan.json

# SOQL クエリの実行
sf data query --query "SELECT Id, Name FROM Account"
```

### Apex 開発

```bash
# Apex クラスの作成
sf apex generate class --name MyClass --output-dir force-app/main/default/classes

# Apex テストの実行
sf apex run test --test-level RunLocalTests --result-format human

# 匿名 Apex の実行
sf apex run --file script.apex
```

## プロジェクト構造

```
my-sfdx-project/
├── sfdx-project.json          # プロジェクト設定ファイル
├── .sfdx/                     # SFDX メタデータ (Git 管理外)
├── .gitignore                 # Git 除外ファイル
├── config/
│   └── project-scratch-def.json  # スクラッチ組織定義
├── force-app/
│   └── main/
│       └── default/
│           ├── classes/       # Apex クラス
│           ├── triggers/      # Apex トリガー
│           ├── lwc/          # Lightning Web Components
│           ├── aura/         # Aura Components
│           ├── objects/      # カスタムオブジェクト
│           ├── tabs/         # タブ
│           ├── layouts/      # ページレイアウト
│           └── ...
└── scripts/
    └── apex/                  # Apex スクリプト
```

## sfdx-project.json の例

```json
{
  "packageDirectories": [
    {
      "path": "force-app",
      "default": true
    }
  ],
  "namespace": "",
  "sfdcLoginUrl": "https://login.salesforce.com",
  "sourceApiVersion": "59.0"
}
```

## project-scratch-def.json の例

```json
{
  "orgName": "My Company",
  "edition": "Developer",
  "features": ["EnableSetPasswordInApi"],
  "settings": {
    "lightningExperienceSettings": {
      "enableS1DesktopEnabled": true
    },
    "mobileSettings": {
      "enableS1EncryptedStoragePref2": false
    }
  }
}
```

## ベストプラクティス

### 1. バージョン管理

- `.gitignore` に `.sfdx/` と `.sf/` を追加
- 認証情報をリポジトリにコミットしない
- 意味のあるコミットメッセージを使用

### 2. スクラッチ組織の管理

- 定期的にスクラッチ組織を再作成して環境をクリーンに保つ
- スクラッチ組織の定義ファイルをバージョン管理
- 開発者ごとに独立したスクラッチ組織を使用

### 3. メタデータの管理

- 小さな変更を頻繁にコミット
- プッシュ/プルの前に変更内容を確認
- コンフリクトは早期に解決

### 4. テスト

- コードカバレッジ 75% 以上を維持
- 単体テストを作成
- 統合テストを実施

### 5. セキュリティ

- 最小権限の原則に従う
- セキュリティレビューを定期的に実施
- CRUD/FLS チェックを実装
- SOQL インジェクション対策

## トラブルシューティング

### 問題: スクラッチ組織が作成できない

**解決策**:

- Dev Hub が有効化されているか確認
- 認証が有効か確認: `sf org list`
- スクラッチ組織の上限に達していないか確認

### 問題: メタデータのプッシュが失敗する

**解決策**:

- エラーメッセージを確認
- 依存関係を確認 (例: カスタムフィールドの前にオブジェクトが必要)
- `sf project deploy start --dry-run` で事前検証

### 問題: 認証の有効期限切れ

**解決策**:

```bash
sf org login web --alias MyOrg
```

## 参考リンク

- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/)
- [Trailhead: Quick Start: Salesforce DX](https://trailhead.salesforce.com/content/learn/projects/quick-start-salesforce-dx)

---

**作成日**: 2026-01-09  
**最終更新日**: 2026-01-09
