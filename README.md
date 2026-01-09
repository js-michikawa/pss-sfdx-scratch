# Salesforce Public Sector Solutions (PSS) - SFDX プロジェクト

## 概要

このプロジェクトは、Salesforce Public Sector Solutions (PSS) の開発環境を SFDX (Salesforce DX) を使用して構築するためのものです。SFDX を活用することで、ソース駆動型の開発、バージョン管理、CI/CD パイプラインの統合が可能になります。

**プロジェクトステータス**: ✅ SFDX プロジェクト初期化済み

## プロジェクトの目的

- **PSS 機能の実装**: 公共部門向けの Salesforce ソリューションを構築
- **カスタマーポータル**: Experience Cloud を使用した市民向けポータル
- **ソース管理**: Git を使用したバージョン管理
- **スクラッチ組織**: 開発用の一時的な Salesforce 環境の作成と管理
- **ベストプラクティス**: Salesforce 開発のベストプラクティスに準拠

## 技術スタック

- **Salesforce CLI (SFDX)**: Salesforce の開発、デプロイ、管理ツール
- **Public Sector Solutions**: Salesforce の公共部門向けソリューション
- **Service Cloud**: ケース管理、オムニチャネル
- **Experience Cloud**: カスタマーポータル
- **OmniStudio**: ローコード開発ツール (FlexCards, OmniScripts)
- **Git**: バージョン管理システム
- **Dev Hub**: スクラッチ組織の管理

## スクラッチ組織の設定内容

このプロジェクトのスクラッチ組織には以下の機能が設定されています:

### 有効化された機能
- ✅ **Public Sector Solutions** - 公共セクターの全機能とオブジェクト
- ✅ **PSS Site Templates** - 助成金管理、ライセンス・許可などの専用テンプレート
- ✅ **Service Cloud** - ケース管理、オムニチャネル
- ✅ **OmniStudio (Runtime & Designer)** - ローコード開発
- ✅ **Experience Cloud** - カスタマーポータル
- ✅ **Knowledge** - ナレッジベース、FAQ
- ✅ **Person Accounts** - 市民の個人情報管理
- ✅ **Multi-Currency** - 複数通貨対応
- ✅ **Omni-Channel** - ケース自動割り当て
- ✅ **Enhanced Notes** - 拡張メモ機能
- ✅ **Path Assistant** - プロセスガイダンス
- ✅ **Chatter** - 内部コラボレーション

詳細は [スクラッチ組織設定ガイド](docs/knowledge/scratch-org-setup.md) を参照してください。

## プロジェクト構造

```
pss-new-scratch/
├── README.md                 # このファイル
├── docs/                     # ドキュメント・ナレッジベース
│   └── knowledge/           # 技術ナレッジ
│       ├── sfdx-basics.md                              # SFDX 基礎
│       ├── pss-development.md                          # PSS 開発ガイド
│       ├── scratch-org-setup.md                        # スクラッチ組織設定
│       └── salesforce-scratch-org-features-reference.md # 公式機能リファレンス
├── force-app/               # Salesforce メタデータ
│   └── main/
│       └── default/
├── config/                  # 設定ファイル
│   └── project-scratch-def.json    # スクラッチ組織定義
├── scripts/                 # スクリプト
│   ├── apex/               # Apex スクリプト
│   └── soql/               # SOQL クエリ
├── sfdx-project.json        # SFDX プロジェクト設定
└── .gitignore              # Git 除外設定
```

## 前提条件

- Salesforce CLI がインストールされていること
- Dev Hub が有効化された Salesforce 組織へのアクセス
- Git がインストールされていること

## セットアップ手順

### 1. Salesforce CLI の確認

```bash
sf --version
```

### 2. Dev Hub への認証

```bash
sf org login web --set-default-dev-hub --alias DevHub
```

### 3. スクラッチ組織の作成

```bash
sf org create scratch --definition-file config/project-scratch-def.json --alias pss-scratch --set-default --duration-days 30
```

### 4. スクラッチ組織を開く

```bash
sf org open
```

### 5. Experience Cloud サイトの作成

スクラッチ組織作成後:
1. Setup > Digital Experiences > All Sites
2. 「New」をクリック
3. テンプレートを選択 (例: Customer Service)
4. サイト名と URL を設定

## 開発ワークフロー

1. **機能開発**: ローカル環境でメタデータを作成・編集
2. **デプロイ**: スクラッチ組織にメタデータをプッシュ
   ```bash
   sf project deploy start
   ```
3. **テスト**: スクラッチ組織で機能をテスト
4. **プル**: 組織で行った変更をローカルに取得
   ```bash
   sf project retrieve start
   ```
5. **コミット**: Git にコミット

## セキュリティ考慮事項

- 認証情報は `.gitignore` に追加し、リポジトリにコミットしない
- 共有設定とプロファイルは最小権限の原則に従う
- データマスキングを使用して本番データを保護
- セキュリティレビューを定期的に実施

## ドキュメント

プロジェクト関連のナレッジとドキュメントは `docs/` ディレクトリに格納されています:

- [SFDX ナレッジベース](docs/knowledge/sfdx-basics.md) - SFDX の基礎知識
- [PSS 開発ガイド](docs/knowledge/pss-development.md) - PSS 開発のベストプラクティス
- [スクラッチ組織設定ガイド](docs/knowledge/scratch-org-setup.md) - スクラッチ組織の設定方法
- [Salesforce 公式機能リファレンス](docs/knowledge/salesforce-scratch-org-features-reference.md) - スクラッチ組織機能の公式ドキュメント

## 参考リンク

- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/)
- [Public Sector Solutions Documentation](https://help.salesforce.com/s/articleView?id=sf.pss_overview.htm)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/)

## ライセンス

このプロジェクトは社内開発用です。

## 貢献

プロジェクトへの貢献は、プルリクエストを通じて行ってください。

---

**最終更新日**: 2026-01-09
