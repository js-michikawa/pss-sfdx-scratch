# Salesforce Public Sector Solutions (PSS) 開発ガイド

## PSS とは

Salesforce Public Sector Solutions (PSS) は、政府機関、教育機関、非営利団体などの公共部門向けに特化した Salesforce のソリューションです。市民サービス、助成金管理、ケース管理、コンプライアンスなどの機能を提供します。

## PSS の主要機能

### 1. 市民サービス管理

- **市民アカウント管理**: 市民の情報を一元管理
- **サービスリクエスト**: 市民からの問い合わせや要求を追跡
- **ケース管理**: 問題解決のワークフロー
- **オムニチャネル対応**: Web、電話、メール、チャットなど複数チャネルでの対応

### 2. 助成金管理

- **助成金プログラム管理**: 助成金プログラムの作成と管理
- **申請プロセス**: オンライン申請フォームとワークフロー
- **審査と承認**: 申請の評価と承認プロセス
- **支払い管理**: 助成金の支払いと追跡
- **レポーティング**: 助成金の使用状況と成果の報告

### 3. 検査・監査管理

- **検査スケジューリング**: 検査の計画と割り当て
- **モバイル検査**: モバイルアプリでの現地検査
- **コンプライアンス追跡**: 規制遵守の監視
- **違反管理**: 違反の記録と是正措置

### 4. ライセンス・許可管理

- **申請管理**: ライセンスや許可の申請処理
- **更新管理**: ライセンスの更新と期限管理
- **手数料管理**: 申請手数料の計算と支払い
- **コンプライアンス**: ライセンス条件の遵守確認

## PSS のデータモデル

### 主要オブジェクト

#### 1. Account (アカウント)

```apex
// PSS では以下のレコードタイプを使用
- Individual (個人)
- Household (世帯)
- Organization (組織)
```

**主要フィールド**:

- `Name`: 名前
- `RecordTypeId`: レコードタイプ
- `PersonEmail`: 個人メールアドレス
- `Phone`: 電話番号

#### 2. Case (ケース)

市民からのサービスリクエストや問い合わせを管理

**主要フィールド**:

- `Subject`: 件名
- `Description`: 詳細
- `Status`: ステータス (New, In Progress, Closed)
- `Priority`: 優先度
- `Origin`: 発生源 (Web, Phone, Email)

#### 3. Grant (助成金) - カスタムオブジェクト

```apex
// 助成金プログラムを管理
Grant__c
```

**主要フィールド**:

- `Name`: 助成金名
- `Program_Name__c`: プログラム名
- `Total_Amount__c`: 総額
- `Start_Date__c`: 開始日
- `End_Date__c`: 終了日
- `Status__c`: ステータス

#### 4. Grant Application (助成金申請) - カスタムオブジェクト

```apex
Grant_Application__c
```

**主要フィールド**:

- `Grant__c`: 助成金 (Lookup)
- `Applicant__c`: 申請者 (Lookup to Account)
- `Requested_Amount__c`: 申請金額
- `Application_Date__c`: 申請日
- `Status__c`: ステータス (Draft, Submitted, Under Review, Approved, Rejected)

## PSS 開発のベストプラクティス

### 1. データモデル設計

- **標準オブジェクトを活用**: 可能な限り標準オブジェクトを使用
- **カスタムオブジェクトの命名規則**: `Object_Name__c` 形式
- **リレーションシップの設計**: Master-Detail vs Lookup を適切に選択
- **データ整合性**: バリデーションルールで整合性を保つ

### 2. セキュリティとプライバシー

- **個人情報保護**: GDPR、CCPA などのコンプライアンス
- **フィールドレベルセキュリティ**: 機密情報へのアクセス制御
- **共有設定**: 組織の共有設定 (OWD) とロールベースの共有
- **監査証跡**: フィールド履歴管理とイベントモニタリング

```apex
// Example: CRUD/FLS check in Apex
if (Schema.sObjectType.Account.isAccessible()) {
    List<Account> accounts = [SELECT Id, Name FROM Account];
}
```

### 3. プロセス自動化

- **Flow**: 宣言的な自動化ツール
  - Screen Flow: ユーザーインタラクション
  - Record-Triggered Flow: レコード変更時の自動化
  - Scheduled Flow: スケジュール実行
- **Process Builder**: 複雑なビジネスプロセス (新規開発では Flow を推奨)
- **Workflow Rules**: シンプルな自動化 (レガシー)

### 4. ユーザーインターフェース

- **Lightning Web Components (LWC)**: モダンな UI コンポーネント
- **Experience Cloud**: 市民向けポータル
- **Mobile**: Salesforce Mobile App のカスタマイズ

### 5. 統合

- **REST API**: 外部システムとの統合
- **SOAP API**: レガシーシステムとの統合
- **Platform Events**: イベント駆動型アーキテクチャ
- **MuleSoft**: エンタープライズ統合プラットフォーム

## PSS 開発ワークフロー

### 1. 要件定義

- ビジネス要件の収集
- ユーザーストーリーの作成
- データモデルの設計

### 2. 設計

- アーキテクチャ設計
- UI/UX デザイン
- セキュリティ設計
- 統合設計

### 3. 開発

```bash
# スクラッチ組織の作成
sf org create scratch --definition-file config/project-scratch-def.json --alias pss-dev

# メタデータの開発
# - Apex クラス
# - Lightning Web Components
# - Flow
# - カスタムオブジェクト

# デプロイ
sf project deploy start

# テスト
sf apex run test --test-level RunLocalTests
```

### 4. テスト

- **単体テスト**: Apex テストクラス (75% 以上のカバレッジ)
- **統合テスト**: エンドツーエンドのシナリオテスト
- **UAT**: ユーザー受け入れテスト
- **パフォーマンステスト**: ガバナ制限の確認

### 5. デプロイ

```bash
# 本番環境へのデプロイ
sf project deploy start --target-org production

# 変更セットの作成 (GUI ベース)
# Setup > Outbound Change Sets
```

## コーディング規約

### Apex

```apex
// Class naming: PascalCase
public class GrantApplicationService {

    // Method naming: camelCase
    public static void processApplication(Id applicationId) {
        // SOQL: Avoid queries in loops
        List<Grant_Application__c> applications = [
            SELECT Id, Status__c, Requested_Amount__c
            FROM Grant_Application__c
            WHERE Id = :applicationId
        ];

        // Null check
        if (applications.isEmpty()) {
            return;
        }

        Grant_Application__c app = applications[0];

        // Business logic
        if (app.Requested_Amount__c > 100000) {
            app.Status__c = 'Requires Additional Review';
        } else {
            app.Status__c = 'Under Review';
        }

        // DML: Bulkify
        update applications;
    }
}
```

### Lightning Web Components

```javascript
// Component naming: camelCase file, PascalCase class
import { LightningElement, api, wire } from "lwc";
import getApplications from "@salesforce/apex/GrantApplicationController.getApplications";

export default class GrantApplicationList extends LightningElement {
  @api recordId;
  applications;
  error;

  @wire(getApplications, { grantId: "$recordId" })
  wiredApplications({ error, data }) {
    if (data) {
      this.applications = data;
      this.error = undefined;
    } else if (error) {
      this.error = error;
      this.applications = undefined;
    }
  }
}
```

## テストコード例

```apex
@isTest
private class GrantApplicationServiceTest {

    @TestSetup
    static void setup() {
        // Create test data
        Grant__c grant = new Grant__c(
            Name = 'Test Grant',
            Total_Amount__c = 500000,
            Status__c = 'Active'
        );
        insert grant;

        Account applicant = new Account(
            Name = 'Test Applicant'
        );
        insert applicant;

        Grant_Application__c app = new Grant_Application__c(
            Grant__c = grant.Id,
            Applicant__c = applicant.Id,
            Requested_Amount__c = 150000,
            Status__c = 'Draft'
        );
        insert app;
    }

    @isTest
    static void testProcessApplication() {
        // Get test data
        Grant_Application__c app = [
            SELECT Id, Requested_Amount__c
            FROM Grant_Application__c
            LIMIT 1
        ];

        // Test
        Test.startTest();
        GrantApplicationService.processApplication(app.Id);
        Test.stopTest();

        // Verify
        app = [
            SELECT Status__c
            FROM Grant_Application__c
            WHERE Id = :app.Id
        ];

        System.assertEquals('Requires Additional Review', app.Status__c);
    }
}
```

## パフォーマンス最適化

### 1. SOQL 最適化

```apex
// Bad: Query in loop
for (Account acc : accounts) {
    List<Contact> contacts = [SELECT Id FROM Contact WHERE AccountId = :acc.Id];
}

// Good: Bulkified query
Map<Id, Account> accountsWithContacts = new Map<Id, Account>([
    SELECT Id, (SELECT Id FROM Contacts)
    FROM Account
    WHERE Id IN :accountIds
]);
```

### 2. DML 最適化

```apex
// Bad: DML in loop
for (Account acc : accounts) {
    update acc;
}

// Good: Bulk DML
update accounts;
```

### 3. ガバナ制限

- SOQL クエリ: 同期 100、非同期 200
- DML ステートメント: 同期 150、非同期 150
- ヒープサイズ: 同期 6MB、非同期 12MB
- CPU 時間: 同期 10,000ms、非同期 60,000ms

## デバッグとトラブルシューティング

### デバッグログの有効化

```bash
# デバッグログの設定
sf apex log get --number 1
```

### Apex デバッガー

- VS Code の Apex Replay Debugger を使用
- ブレークポイントの設定
- 変数の検査

### エラーハンドリング

```apex
try {
    // Risky operation
    insert applications;
} catch (DmlException e) {
    // Log error
    System.debug('Error: ' + e.getMessage());
    // Handle error gracefully
    for (Integer i = 0; i < e.getNumDml(); i++) {
        System.debug('Error on record ' + i + ': ' + e.getDmlMessage(i));
    }
}
```

## 参考リンク

- [Public Sector Solutions Documentation](https://help.salesforce.com/s/articleView?id=sf.pss_overview.htm)
- [Apex Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/)
- [Lightning Web Components Developer Guide](https://developer.salesforce.com/docs/component-library/documentation/en/lwc)
- [Salesforce Security Guide](https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/)

---

**作成日**: 2026-01-09  
**最終更新日**: 2026-01-09
