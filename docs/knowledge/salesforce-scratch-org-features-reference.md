元のページのURL
https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm


# スクラッチ組織の機能

スクラッチ組織定義には、スクラッチ組織の具体的な形を決める設定値が含まれます。スクラッチ組織では次のサポートされているアドオン機能を有効にできます。



メモ

スクラッチ組織の機能の中には、Dev Hub 組織のライセンスや権限が必要なものがあります。スクラッチ組織定義ファイルに機能名を指定するだけではスクラッチ組織を作成できない場合は、Salesforce のシステム管理者にお問い合わせください。

## サポートされる機能

機能では、大文字と小文字は区別されません。すべて大文字で指定することも、ここで定義するように読みやすく指定することもできます。機能の後に <値> が続いている場合、増分割り当てまたは制限としての値を指定する必要があります。

スクラッチ組織定義ファイルには、カンマ区切りリストで複数の機能値を指定できます。

```
"features": ["ServiceCloud", "API", "AuthorApex"],
```

- **[AccountInspection](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_accountinspection)**
  取引先インテリジェンスビューを有効にします。取引先インテリジェンスビューは、取引先の総計値、活動、関連する商談やケースを表示する統合ダッシュボードです。
- **[AccountingSubledgerGrowthEdition](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_accountingsubledgergrowthedition)**
  会計補助台帳拡張機能へのアクセスを可能にする 3 つの権限セットが提供されます。
- **[AccountingSubledgerStarterEdition](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_accountingsubledgerstarteredition)**
  会計補助台帳スターター機能へのアクセスを可能にする 3 つの権限セットが提供されます。
- **[AccountingSubledgerUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_accountingsubledgeruser)**
  パッケージのインストール時に会計補助台帳拡張機能への組織のアクセスを有効にします。
- **[AddCustomApps:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_addcustomapps)**
  組織で使用できるカスタムアプリケーションの最大数を増やします。1 ～ 30 の値を指定します。
- **[AddCustomObjects:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_addcustomobjects)**
  組織で使用できるカスタムオブジェクトの最大数を増やします。1 ～ 30 の値を指定します。
- **[AddCustomRelationships:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_addcustomrelationships)**
  オブジェクトで使用できるカスタムリレーションの最大数を増やします。1 ～ 10 の値を指定します。
- **[AddCustomTabs:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_addcustomtabs)**
  組織で使用できるカスタムタブの最大数を増やします。1 ～ 30 の値を指定します。
- **[AddDataComCRMRecordCredit:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_adddatacomcrmrecordcredit)**
  スクラッチ組織のユーザーに割り当てられる、レコードをインポートするためのクレジット数を増やします。1 ～ 30 の値を指定します。
- **[AddInsightsQueryLimit:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_addinsightsquerylimit)**
  CRM Analytics のクエリ結果のサイズを増やします。1 ～ 30 の値を指定します (乗数は 10)。数量を 6 に設定するとクエリ結果が 60 に増加します。
- **[AdditionalFieldHistory:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_additionalfieldhistory)**
  履歴を追跡できる項目数をデフォルトの 20 項目から増やします。1 ～ 40 の値を指定します。
- **[AdmissionsConnectUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_admissionsconnectuser)**
  Admissions Connect コンポーネントを有効化します。このスクラッチ組織の機能パラメーターがない場合、カスタム Admissions Connect コンポーネントは空白でレンダリングされます。
- **[AdvisorLinkFeature](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_advisorlinkfeature)**
  Student Success Hub コンポーネントを有効化します。このスクラッチ組織の機能パラメーターがない場合、カスタム Student Success Hub コンポーネントは空白でレンダリングされます。
- **[AdvisorLinkPathwaysFeature](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_advisorlinkpathwaysfeature)**
  Pathways コンポーネントを有効化します。このスクラッチ組織の機能パラメーターがない場合、カスタム Pathways コンポーネントは空白でレンダリングされます。
- **[AIAttribution](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_aiattribution)**
  Marketing Cloud Account Engagement 用 Einstein 属性へのアクセス権の提供。Einstein 属性は、AI モデリングを使用して、複数のキャンペーンタッチポイントに動的に属性のパーセントを割り当てます。
- **[AnalyticsAdminPerms](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_analyticsadminperms)**
  CRM Analytics テンプレートアプリケーションや CRM Analytics アプリケーションの作成を可能にする権限など、CRM Analytics プラットフォームの管理に必要なすべての権限を有効にします。
- **[AnalyticsAppEmbedded](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_analyticsappembedded)**
  CRM Analytics プラットフォーム用の CRM Analytics Embedded App ライセンスを 1 つ提供します。
- **[API](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_api)**
  API アクセス権が提供されないエディション (Professional、Group) であっても、REST API はデフォルトで有効になっています。このスクラッチ組織の機能を使用して、追加の API (SOAP、ストリーミング、Bulk、Bulk 2.0) にアクセスします。
- **[ArcGraphCommunity](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_arcgraphcommunity)**
  Experience Cloud ページに Actionable Relationship Center (ARC) コンポーネントを追加することで、ユーザーが ARC リレーショングラフを表示できるようになります。
- **[評価](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_assessments)**
  動的評価機能を有効にします。これにより、評価の質問と評価の質問セットの両方が有効になります。
- **[AssetScheduling:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_assetscheduling)**
  Asset Scheduling ライセンスを有効にします。アセットのスケジュールにより、部屋と機器を簡単に予約できます。1 ～ 10 の値を指定します。
- **[AssociationEngine](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_associationengine)**
  関連付けエンジンを有効化します。これにより支店ユニット顧客レコードを作成することで、新しい取引先がユーザーの現在の支店に自動的に関連付けられます。
- **[AuthorApex](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_authorapex)**
  スクラッチ組織で Apex コードにアクセスして変更できるようにします。Enterprise Edition と Developer Edition ではデフォルトで有効になっています。
- **[B2BCommerce](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_b2bcommerce)**
  B2B ライセンスを提供します。B2BCommerce により、組織で企業間 (B2B) 取引が可能になります。B2B ストアを作成および更新します。バイヤーアカウントを作成および管理します。商品を他の企業に販売します。
- **[B2BLoyaltyManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_b2bloyaltymanagement)**
  B2B Loyalty Management ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。
- **[B2CCommerceGMV](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_b2ccommercegmv)**
  B2B2C Commerce ライセンスを提供します。B2B2C Commerce では、e コマースサイトを迅速に立ち上げ、複数のデジタルチャネルでブランドのプロモーションや製品の販売を行うことができます。組織の小売ストアフロントの作成や更新、個人取引先の作成や管理が可能です。
- **[B2CLoyaltyManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_b2cloyaltymanagement)**
  Loyalty Management - Growth ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。
- **[B2CLoyaltyManagementPlus](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_b2cloyaltymanagementplus)**
  Loyalty Management - Advanced ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。
- **[BatchManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_batchmanagement)**
  Batch Management ライセンスを有効にします。一括管理により、管理しやすいバッチで大量のレコードを処理できます。
- **[BigObjectsBulkAPI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_bigobjectsbulkapi)**
  スクラッチ組織が Bulk API で BigObjects を使用できるようにします。
- **[ブリーフケース](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_briefcase)**
  スクラッチ組織でブリーフケースビルダーを使用できるようにします。これにより、オフラインブリーフケースを作成し、選択したレコードをオフラインで表示できるようになります。
- **[BudgetManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_budgetmanagement)**
  予算管理機能とオブジェクトへのアクセス権をユーザーに付与します。予算管理機能を有効にするには、この機能をスクラッチ組織定義ファイルに追加します。
- **[BusinessRulesEngine](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_businessrulesengine)**
  ビジネスルールエンジンを有効化します。これにより、式セットとルックアップテーブルの両方が有効化されます。
- **[CacheOnlyKeys](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cacheonlykeys)**
  キャッシュのみの鍵サービスを有効にします。この機能では、Salesforce 外部の鍵素材を保存したり、キャッシュのみの鍵サービスを使用して、制御する鍵サービスからオンデマンドで鍵を取得したりできます。
- **[CalloutSizeMB:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_calloutsizemb)**
  Apex コールアウトの最大サイズを増やします。3 ～ 12 の値を指定します。
- **[CampaignInfluence2](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_campaigninfluence2)**
  Sales Cloud と Marketing Cloud Account Engagement でのカスタマイズ可能なキャンペーンインフルエンスへのアクセスを提供します。カスタマイズ可能なキャンペーンインフルエンスでは、属性を追跡するために、キャンペーンと商談間のリレーションを自動的に関連付けたり、手動で作成したりできます。
- **[CascadeDelete](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cascadedelete)**
  以前は主従関係でのみ使用できたカスケード削除機能を、ルックアップリレーションでも使用できるようにします。レコードが誤って削除されないようにするため、デフォルトではカスケード削除は無効になっています。
- **[CaseClassification](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_caseclassification)**
  Einstein ケース分類を有効にします。ケース分類は、エージェントが最適な値を選択できるように、おすすめを提供します。また、自動的に最適なおすすめを保存して、ケースを適切なエージェントにルーティングすることもできます。
- **[CaseWrapUp](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_casewrapup)**
  Einstein ケースラップアップを有効にします。エージェントがすばやくケースを完了できるように、Einstein ケースラップアップが過去のチャットトランスクリプトに基づいてケース項目値を推奨します。
- **[ChangeDataCapture](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_changedatacapture)**
  スクラッチ組織のエディションで変更データキャプチャが自動的に有効にならない場合に、変更データキャプチャを有効にします。
- **[Chatbot](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_chatbot)**
  ボットメタデータをスクラッチ組織にリリースして、ボットを作成および編集できるようにします。
- **[ChatterEmailFooterLogo](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_chatteremailfooterlogo)**
  ChatterEmailFooterLogo により、ロゴ画像のドキュメント ID を使用して Chatter メールをカスタマイズできます。
- **[ChatterEmailFooterText](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_chatteremailfootertext)**
  ChatterEmailFooterText により、カスタム Chatter メールでフッターテキストを使用できるようになります。
- **[ChatterEmailSenderName](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_chatteremailsendername)**
  ChatterEmailSenderName により、メール通知の送信者名として表示される名前をカスタマイズできます。たとえば、会社の名前を指定できます。
- **[CloneApplication](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cloneapplication)**
  CloneApplication により、既存のカスタム Lightning アプリケーションをコピーして、その新しいアプリケーションで必要なカスタマイズを行うことができます。この方法によってゼロから始める必要がなくなり、特に簡単なバリエーションのアプリケーションを作成するときに役立ちます。
- **[CMSMaxContType](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cmsmaxconttype)**
  Salesforce CMS で作成できる個別のコンテンツ種別の数を 21 に制限します。
- **[CMSMaxNodesPerContType](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cmsmaxnodesperconttype)**
  特定のコンテンツ種別に対して作成できる子ノード (項目) の最大数を 15 に制限します。
- **[CMSUnlimitedUse](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cmsunlimiteduse)**
  Salesforce CMS でのコンテンツレコード数、コンテンツ種別数、帯域幅の使用を無制限にします。
- **[コミュニティ](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_communities)**
  組織でカスタマーコミュニティを作成できるようにします。コミュニティを使用するには、スクラッチ組織定義ファイルの設定セクションに [communitiesSettings] > [enableNetworksEnabled] を含める必要もあります。
- **[ConAppPluginExecuteAsUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_conapppluginexecuteasuser)**
  ConnectedApp メタデータ API オブジェクトで pluginExecutionUser 項目を有効にします。
- **[ConcStreamingClients:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_concstreamingclients)**
  API バージョン 36.0 以前のすべてのチャネルとすべてのイベント種別での、同時クライアント (登録者) の最大数を増やします。20 ～ 4,000 の値を指定します。
- **[ConnectedAppCustomNotifSubscription](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_connectedappcustomnotifsubscription)**
  接続アプリケーションを有効化して、カスタムデスクトップおよびモバイルの通知を送信するために使用するカスタム通知種別を登録できるようにします。
- **[ConnectedAppToolingAPI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_connectedapptoolingapi)**
  Tooling API で接続アプリケーションを使用できるようにします。
- **[ConsentEventStream](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_consenteventsstream)**
  組織で「Consent Event Stream (同意イベントストリーム)」権限を有効にします。
- **[ConsolePersistenceInterval:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_consolepersistenceinterval)**
  コンソールデータを保存する頻度を分単位で増やします。0 ～ 500 の値を指定します。自動保存を無効にするには値を 0 に設定します。
- **[ContactsToMultipleAccounts](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_contactstomultipleaccounts)**
  取引先責任者-to-複数取引先機能を有効化します。この機能により、1 人の取引先責任者を複数の取引先に関連付けることができます。
- **[ContractApprovals](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_contractapprovals)**
  取引先責任者の承認を有効化して、承認プロセスを通して契約を追跡できるようにします。
- **[ContractManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_contractmanagement)**
  組織で契約ライフサイクル管理 (CLM) 機能を有効にします。
- **[ContractMgmtInd](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_contractmgmtind)**
  業種の契約ライフサイクル管理 (CLM) 機能を有効にします。
- **[CPQ](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_cpq)**
  Salesforce CPQ 管理パッケージのインストールに必要なライセンス機能が有効化されますが、パッケージは自動的にインストールされません。
- **[CustomFieldDataTranslation](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_customfielddatatranslation)**
  ユーザーが作業種別グループオブジェクト、サービステリトリーオブジェクト、サービスリソースオブジェクトのカスタム項目データの翻訳を可能にします。テキスト型、テキストエリア型、ロングテキストエリア型、テキストエリア (リッチ) 型、および URL 型のカスタム項目のデータ翻訳を有効にできます。
- **[CustomNotificationType](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_customnotificationtype)**
  カスタムデスクトップおよびモバイル通知を送信するために使用するカスタム通知タイプを組織で作成できるようにします。
- **[DataComDnbAccounts](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_datacomdnbaccounts)**
  Data.com 取引先機能のライセンスを提供します。
- **[DataComFullClean](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_datacomfullclean)**
  Data.com クリーニング機能のライセンスを提供し、ジョブの自動入力クリーンアップ設定を有効にします。
- **[DataMaskUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_datamaskuser)**
  30 件の Data Mask 権限セットライセンスを提供します。この権限セットにより、インストールされている Salesforce Data Mask パッケージにアクセスできるようになります。
- **[DataProcessingEngine](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_dataprocessingengine)**
  Data Processing Engine ライセンスを有効にします。データ処理エンジンでは、Salesforce 組織で使用可能なデータを変換し、その結果を新規レコードまたは更新レコードとして書き戻すことができます。
- **[DebugApex](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_debugapex)**
  Apex 対話型デバッガーを有効にします。このデバッガーを使用すると、ブレークポイントとチェックポイントを設定して Apex コードをデバッグし、コードからバグを見つけることができます。
- **[DecisionTable](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_decisiontable)**
  Decision Table ライセンスを有効にします。決定表はビジネスルールを読み取り、Salesforce 組織内のレコードまたは指定した値の結果を決定します。
- **[DefaultWorkflowUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_defaultworkflowuser)**
  スクラッチ組織の管理者をデフォルトのワークフローユーザーとして設定します。
- **[DeferSharingCalc](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_defersharingcalc)**
  グループメンバーシップとルール計算の共有を一時的に停止して、後で再開できるようにします。
- **[DevelopmentWave](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_developmentwave)**
  スクラッチ組織で CRM Analytics 開発を有効にします。5 件のプラットフォームライセンスと 5 件の CRM Analytics プラットフォームライセンスを組織に割り当て、権限セットライセンスを管理ユーザーに割り当てます。CRM Analytics テンプレートと Einstein Discovery 機能も有効にします。
- **[DeviceTrackingEnabled](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_devicetrackingenabled)**
  デバイス追跡を有効にします。
- **[DevOpsCenter](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_devopscenter)**
  スクラッチ組織の DevOps センターを有効にします。これにより、パートナーは、DevOps センターアプリケーション (基本) パッケージの機能を拡張、強化する第二世代管理パッケージを作成できるようになります。
- **[DisableManageIdConfAPI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_disablemanageidconfapi)**
  LoginIP オブジェクトと ClientBrowser API オブジェクトへのアクセスを制限して、表示と削除のみを可能にします。
- **[DisclosureFramework](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_disclosureframework)**
  開示とコンプライアンスのハブの設定に必要な権限セットライセンスと権限セットを提供します。
- **[Division](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_division)**
  [会社の設定] の [ディビジョンの管理] を有効にします。ディビジョンでは、組織のデータを論理セクションに分類できます。これにより、検索、レポート、およびリストビューがユーザーにとってより有用となります。ディビジョンは、データ量が極めて多い組織に有用です。
- **[DocGen](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_docgen)**
  組織でドキュメント生成機能を有効にします。
- **[DocGenDesigner](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_docgendesigner)**
  ドキュメントテンプレートの作成および定義を行うためのデザイナーを有効にします。
- **[DocGenInd](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_docgenind)**
  組織で業種のドキュメント生成機能を有効にします。
- **[DocumentChecklist](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_documentchecklist)**
  ドキュメントの追跡と承認機能を有効にして、「ドキュメントチェックリスト」権限セットを追加します。ドキュメント追跡機能により、アップロードして承認するドキュメントを定義して、ローン申請などのプロセスやアクションプランをサポートできます。
- **[DocumentReaderPageLimit](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_documentreaderpagelimit)**
  データ抽出のために送信されるページ数を 5 に制限します。
- **[DSARPortability](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_dsarportability)**
  組織でのプライバシーセンターの DSARPortability 機能へのアクセスを有効にします。また、PrivacyCenter ライセンスと PrivacyCenterAddOn ライセンスのシートがそれぞれ 1 個提供されます。
- **[DurableClassicStreamingAPI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_durableclassicstreamingapi)**
  API バージョン 37.0 以降のデュラブル PushTopic ストリーミング API を有効にします。
- **[DurableGenericStreamingAPI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_durablegenericstreamingapi)**
  API バージョン 37.0 以降のデュラブル汎用ストリーミング API を有効にします。
- **[DynamicClientCreationLimit](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_dynamicclientcreationlimit)**
  組織で動的クライアント登録エンドポイントを使用して最大 100 件の OAuth 2.0 接続アプリケーションを登録できるようにします。
- **[EAndUDigitalSales](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_eandudigitalsales)**
  組織でエネルギーおよび公益事業のデジタルセールス機能を有効にします。
- **[EAndUSelfServicePortal](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_eanduselfserviceportal)**
  組織で、デジタルエクスペリエンスユーザーのセルフサービスポータル機能を有効にします。
- **[EAOutputConnectors](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_eaoutputconnectors)**
  CRM Analytics 出力コネクタを有効化します。
- **[EASyncOut](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_easyncout)**
  CRM Analytics SyncOut を有効にします。
- **[EdPredictionM3Threshold](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_edpredictionm3threshold)**
  ペイロードのレコード数を 10 に設定します。それ以降、Einstein Discovery 予測サービスは M3 を使用します。
- **[EdPredictionTimeout](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_edpredictiontimeout)**
  1 つの Einstein Discovery 予測の最大継続時間を 100 ミリ秒に設定します。
- **[EdPredictionTimeoutBulk](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_edpredictiontimeoutbulk)**
  Einstein Discovery 予測を一括で実行する際の 1 つの Einstein Discovery 予測の最大継続時間を 10 ミリ秒に設定します。
- **[EdPredictionTimeoutByomBulk](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_edpredictiontimeoutbyombulk)**
  Bring Your Own Model (BYOM) の 1 つの Einstein Discovery 予測の最大継続時間を 100 ミリ秒に設定します。
- **[EducationCloud: ](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_educationcloud)**
  Education Cloud を使用できるようにします。
- **[EinsteinAnalyticsPlus](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinanalyticsplus)**
  CRM Analytics プラットフォーム用の CRM Analytics Plus ライセンスを 1 つ提供します。
- **[EinsteinArticleRecommendations](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinarticlerecommendations)**
  Einstein 記事のおすすめのライセンスを提供します。Einstein 記事のおすすめでは、過去のケースのデータを使用して、カスタマーサービスエージェントが顧客からの問い合わせに対応するのに最も役立ちそうなナレッジ記事を識別します。
- **[EinsteinBuilderFree](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinbuilderfree)**
  システム管理者が Einstein 予測ビルダーで 1 件の有効な予測を作成できるようにするライセンスを提供します。Einstein 予測ビルダーは、システム管理者向けのカスタム AI です。
- **[EinsteinDocReader](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteindocreader)**
  インテリジェントフォームリーダーをスクラッチ組織で有効化および使用するために必要なライセンスを提供します。インテリジェントフォームリーダーは光学式文字認識と Amazon Textract を使用してデータを自動に抽出します。
- **[EinsteinRecommendationBuilder](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinrecommendationbuilder)**
  Einstein レコメンデーションビルダーでおすすめを作成するためのライセンスを提供します。Einstein レコメンデーションビルダーではカスタム AI レコメンデーションを構築できます。
- **[EinsteinRecommendationBuilderMetadata](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinrecommendationbuildermetadata)**
  Einstein レコメンデーションビルダーが必要なメタデータ API を使用できるようにします。この機能を有効にすると、カスタム AI レコメンデーションを構築できます。
- **[EinsteinSearch](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinsearch)**
  スクラッチ組織で Einstein Search 機能を使用および有効化するために必要なライセンスを提供します。
- **[EinsteinVisits](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinvisits)**
  Consumer Goods Cloud を有効にします。Consumer Goods Cloud を使用すると、小売チャネルパートナーとのコラボレーション方法が変わります。営業マネージャーは、訪問を計画し、店舗をまたがってビジネスの健全性を分析できます。また、フィールド営業担当者は、リテールエグゼキューションモバイルアプリケーションを使用して在庫を追跡し、注文を受け付け、訪問の詳細を記録できます。
- **[EinsteinVisitsED](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_einsteinvisitsed)**
  Einstein Discovery を有効化します。Einstein Discovery は、店舗訪問レコメンデーションを取得する場合に使用します。Einstein 訪問 ED を使用すると訪問頻度戦略を作成することができ、これにより Einstein は、最適な店舗訪問レコメンデーションを提供できます。
- **[EmbeddedLoginForIE](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_embeddedloginforie)**
  IE11 で組み込みログインをサポートする JavaScript ファイルを提供します。
- **[EmpPublishRateLimit:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_emppublishratelimit)**
  毎時公開される標準量のプラットフォームイベント通知の最大数を増やします。1,000 ～ 10,000 の値を指定します。
- **[EnablePRM](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_enableprm)**
  組織でパートナーリレーション管理権限を有効にします。
- **[EnableManageIdConfUI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_enablemanageidconfui)**
  LoginIP オブジェクトと ClientBrowser API オブジェクトにアクセスして、UI でユーザーの ID を検証できるようにします。
- **[EnableSetPasswordInApi](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_enablesetpasswordinapi)**
  sf org generate password を使用して、古いパスワードを入力せずにパスワードを変更できるようにします。
- **[EncryptionStatisticsInterval:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_encryptionstatisticsinterval)**
  暗号化統計収集プロセスの間隔 (秒単位) を定義します。最大値は 604,800 秒 (7 日) です。デフォルトは 86,400 秒 (24 時間) に 1 回です。
- **[EncryptionSyncInterval:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_encryptionsyncinterval)**
  組織がデータを有効な鍵素材と同期できる頻度 (秒単位) を定義します。デフォルト値は、最大値の 604,800 秒 (7 日) です。データの同期頻度を高めるには、0 以上の秒単位の値を指定します。
- **[EnergyAndUtilitiesCloud](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_energyandutilitiescloud)**
  組織で、Energy and Utilities Cloud 機能を有効にします。
- **[エンタイトルメント](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_entitlements)**
  エンタイトルメントの有効化。エンタイトルメントは、サービス契約の利用規約を表す Salesforce のカスタマーサポートのユニット (「電話サポート」や「Web サポート」など) です。
- **[EventLogFile](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_eventlogfile)**
  組織のイベントログファイルへの API アクセスを有効にします。イベントモニタリング製品では、Salesforce 組織の操作イベントに関する情報を収集します。この情報を使用して、利用状況のトレンドやユーザーの操作を分析できます。
- **[EntityTranslation](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_entitytranslation)**
  ユーザーが作業種別グループオブジェクト、サービステリトリーオブジェクト、サービスリソースオブジェクトの項目データの翻訳を可能にします。
- **[ExpressionSetMaxExecPerHour](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_expressionsetmaxexecperhour)**
  Connect REST API を使用することで、組織では 1 時間あたり最大 50 万の式セットを実行できるようになります。
- **[ExternalIdentityLogin](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_externalidentitylogin)**
  スクラッチ組織で外部 ID ライセンスに関連付けられている Salesforce Customer Identity 機能を使用できるようにします。
- **[FieldAuditTrail](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldaudittrail)**
  組織で項目監査履歴を有効にして、60 件までの項目を追跡できるようにします。デフォルトでは 20 件の項目がすべての組織で追跡され、項目監査履歴ではさらに 40 件の項目が追跡されます。
- **[FieldService:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldservice)**
  Field Service ライセンスを提供します。1 ～ 25 の値を指定します。
- **[FieldServiceAppointmentAssistantUser:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldserviceappointmentassistantuser)**
  Field Service 予定アシスタントの権限セットライセンスを追加します。1 ～ 25 の値を指定します。
- **[FieldServiceDispatcherUser:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldservicedispatcheruser)**
  Field Service Dispatcher 権限セットライセンスを追加します。1 ～ 25 の値を指定します。
- **[FieldServiceLastMileUser:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldservicelastmileuser)**
  Field Service Last Mile 権限セットライセンスを追加します。1 ～ 25 の値を指定します。
- **[FieldServiceMobileExtension](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldservicemobileextension)**
  Field Service Mobile Extension 権限セットライセンスを追加します。
- **[FieldServiceMobileUser:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldservicemobileuser)**
  Field Service Mobile 権限セットライセンスを追加します。1 ～ 25 の値を指定します。
- **[FieldServiceSchedulingUser:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fieldserviceschedulinguser)**
  Field Service Scheduling 権限セットライセンスを追加します。1 ～ 25 の値を指定します。
- **[FinanceLogging](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_financelogging)**
  ファイナンスログオブジェクトをスクラッチ組織に追加します。この機能は、ファイナンスログのために必要です。
- **[FinancialServicesCommunityUser:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_financialservicescommunityuser)**
  「Financial Services 保険コミュニティ」権限セットライセンスを追加し、Financial Services 保険コミュニティのコンポーネントとオブジェクトにアクセスできるようにします。1 ～ 10 の値を指定します。
- **[FinancialServicesInsuranceUser:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_financialservicesinsuranceuser)**
  「Financial Services 保険」権限セットライセンスを追加し、Financial Services 保険のコンポーネントとオブジェクトにアクセスできるようにします。1 ～ 10 の値を指定します。
- **[FinancialServicesUser:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_financialservicesuser)**
  Financial Services Cloud の標準権限セットライセンスを追加します。この権限セットは、Lightning コンポーネントおよび Financial Services Cloud の標準バージョンにアクセスできるようにします。また、Salesforce の標準オブジェクトおよびカスタム Financial Services Cloud オブジェクトにもアクセスできるようにします。1 ～ 10 の値を指定します。
- **[FlowSites](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_flowsites)**
  Salesforce サイトとカスタマーポータルでフローを使用できるようにします。
- **[ForceComPlatform](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_forcecomplatform)**
  1 件の Salesforce Platform ユーザーライセンスを追加します。
- **[ForecastEnableCustomField](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_forecastenablecustomfield)**
  商談に基づいた予測でカスタム通貨と顧客番号の項目を総計値として使用できるようにします。
- **[FSCAlertFramework](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fscalertframework)**
  スクラッチ組織で、Financial Services Cloud レコードアラートエンティティにアクセスできるようにします。
- **[FSCServiceProcess](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fscserviceprocess)**
  Financial Services Cloud のサービスプロセススタジオ機能を有効化します。IndustriesServiceExcellenceAddOn ライセンスと FinancialServicesCloudStardardAddOn ライセンスのシートをそれぞれ 10 個提供します。この機能を有効にするには、[設定] で StandardServiceProcess 設定をオンにし、ユーザーに AccessToServiceProcess 権限を付与する必要もあります。
- **[資金調達](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_fundraising)**
  Nonprofit Cloud for Fundraising 機能とオブジェクトへのアクセス権をユーザーに付与します。
- **[GenericStreaming](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_genericstreaming)**
  API バージョン 36.0 以前の汎用ストリーミング API を有効にします。
- **[GenStreamingEventsPerDay:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_genstreamingeventsperday)**
  API バージョン 36.0 以前の汎用ストリーミングを使用した場合の、24 時間以内に配信され、すべての CometD クライアントで共有されるイベント通知の最大数を増やします。10,000 ～ 50,000 の値を指定します。
- **[助成金提供](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_grantmaking)**
  Salesforce および Experience Cloud で助成金提供機能およびオブジェクトへのアクセス権をユーザーに付与します。
- **[HealthCloudAddOn](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_healthcloudaddon)**
  Health Cloud を使用できるようにします。
- **[HealthCloudEOLOverride](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_healthcloudeoloverride)**
  Salesforce は Spring ‘22 でより堅牢なリードオブジェクトに集中するため、Health Cloud CandidatePatient オブジェクトを廃止しました。このスクラッチ組織の機能では、その廃止を上書きしてこのオブジェクトにアクセスできます。
- **[HealthCloudForCmty](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_healthcloudforcmty)**
  Experience Cloud サイトでの Health Cloud の使用を有効にします。
- **[HealthCloudMedicationReconciliation](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_healthcloudmedicationreconciliation)**
  薬剤管理で薬剤確認をサポートできるようにします。
- **[HealthCloudPNMAddOn](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_healthcloudpnmaddon)**
  プロバイダーネットワーク管理の使用を有効にします。
- **[HealthCloudUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_healthclouduser)**
  これによりスクラッチ組織は、1 人のユーザーの Health Cloud 権限セットライセンスと同等の Health Cloud オブジェクトおよび機能を使用できます。
- **[HighVelocitySales](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_highvelocitysales)**
  Sales Engagement ライセンスを提供し、Salesforce Inbox を有効にします。Sales Engagement は、生産性の高いワークスペースを使用して、インサイドセールスプロセスを最適化します。営業マネージャーは、さまざまな種別の見込み客を処理する方法を営業担当に示す、カスタムセールスプロセスを作成できます。営業担当は、優先リストや他の生産性向上機能によって見込み客をすばやく処理できます。Sales Engagement 機能はスクラッチ組織にリリースできますが、機能の設定はスクラッチ組織定義ファイルを介して更新できません。代わりに、Sales Engagement アプリケーションで設定を直接定義します。
- **[HoursBetweenCoverageJob:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_hoursbetweencoveragejob)**
  オブジェクトに対して共有継承の対象範囲レポートを実行する頻度 (時単位)。1 ～ 24 の値を指定します。
- **[IdentityProvisioningFeatures](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_identityprovisioningfeatures)**
  Salesforce Identity のユーザープロビジョニングを使用できるようにします。
- **[IgnoreQueryParamWhitelist](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_ignorequeryparamwhitelist)**
  クエリパラメーターの絞り込みルールで許可リストルールを無視します。有効である場合は、URL に任意のクエリパラメーターを追加できます。
- **[IndustriesActionPlan](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_industriesactionplan)**
  アクションプランのライセンスを提供します。アクションプランにより、ビジネスプロセスを完了するための ToDo やドキュメントチェックリスト項目を定義できます。
- **[IndustriesBranchManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_industriesbranchmanagement)**
  支店管理を使用することで、支店のマネージャーと管理者は Financial Services Cloud で支店、従業員、および顧客セグメントの仕事の成果を追跡できます。
- **[IndustriesCompliantDataSharing](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_industriescompliantdatasharing)**
  参加者管理や、データ共有の高度な設定へのアクセス権をユーザーに付与することで、規制や会社のポリシーへの準拠を強化します。
- **[IndustriesMfgTargets](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_industriesmanufacturing)**
  販売計画を有効にします。販売計画を使用すると、継続的な期間にわたって商品の購入および販売に関する交渉を行うことができます。また、商品、価格、割引、数量に関するインサイトを得ることができます。さらに、注文と契約からのリアルタイム更新を使用して計画数、実績数、および収益を追跡することもできます。
- **[IndustriesManufacturingCmty](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_industriesmanufacturingcmty)**
  パートナーコミュニティユーザーによる使用を目的とした「コミュニティの製造販売計画」権限セットライセンスを提供します。また、システム管理者がコミュニティを作成するための製造業コミュニティテンプレートにもアクセスできるようにします。
- **[IndustriesMfgAccountForecast](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_industriesmfgaccountforecast)**
  取引先販売予測を有効にします。取引先販売予測により、注文、商談、販売計画に基づいて、取引先の販売予測を生成できます。また、取引先販売予測を使用することで、会社の要件に従って、販売予測を計算する数式を作成できます。
- **[InsightsPlatform](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_insightsplatform)**
  CRM Analytics 用の CRM Analytics Plus ライセンスを有効にします。
- **[InsuranceCalculationUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_insurancecalculationuser)**
  保険の計算機能を有効にします。BRERuntimeAddOn ライセンスと OmniStudioRuntime ライセンスのシートをそれぞれ 10 個提供します。また、OmniStudio ライセンスと BREPlatformAccess ライセンスのシートをそれぞれ 1 個提供します。
- **[InsuranceClaimMgmt](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_insuranceclaimmgmt)**
  請求管理機能を有効にします。InsuranceClaimMgmtAddOn ライセンスのシートを 1 個提供します。
- **[InsurancePolicyAdmin](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_insurancepolicyadmin)**
  保険契約管理機能を有効にします。InsurancePolicyAdministrationAddOn ライセンスのシートを 1 個提供します。
- **[IntelligentDocumentReader](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_intelligentdocumentreader)**
  インテリジェントドキュメントリーダーをスクラッチ組織で有効化および使用するために必要なライセンスを提供します。インテリジェントドキュメントリーダーは、AWS アカウントを使用して Amazon Textract で光学式文字認識を使ってデータを自動抽出します。
- **[Interaction](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_interaction)**
  フローを有効にします。フローは、Salesforce 組織または外部システム内でデータを収集し、アクションを実行する Salesforce フローの一部です。Salesforce フローでは、画面フローと自動起動フローの 2 種類のフローが提供されます。
- **[IoT](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_iot)**
  IoT を有効にして、スクラッチ組織がプラットフォームイベントを消費してオーケストレーションとコンテキストを使用したビジネスワークフローとサービスワークフローを実行できるようにします。
- **[JigsawUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_jigsawuser)**
  Jigsaw 機能のライセンスを 1 件提供します。
- **[ナレッジ](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_knowledge)**
  Salesforce ナレッジを有効にして、Web サイト訪問者、クライアント、パートナー、およびサービスエージェントに最上級のサポートを提供できるようにします。自社の情報を使用した知識ベースを作成して管理し、必要な時に必要な場所で安全に共有します。製品をデフォルトに戻す方法などのプロセスに関連した情報やよくある質問などを掲載した記事の知識ベースを構築してください。
- **[LegacyLiveAgentRouting](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_legacyliveagentrouting)**
  チャットで従来の Live Agent ルーティングを有効にします。Salesforce Classic で Live Agent ルーティングを使用してチャットを行います。Lightning Experience のチャットでは、オムニチャネルを使用したルーティングが必要です。
- **[LightningSalesConsole](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_lightningsalesconsole)**
  Lighting Sales Console ユーザーライセンスを 1 件追加します。
- **[LightningScheduler](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_lightningscheduler)**
  Lightning Scheduler を有効にします。Lightning Scheduler は、Salesforce での予定のスケジュールを簡略化するためのツールを提供します。適切な担当者が割り当てられた顧客の予定 (対面、電話、またはビデオチャット) を適切な場所と時間にスケジュールすることで、パーソナライズした環境を作成します。
- **[LightningServiceConsole](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_lightningserviceconsole)**
  Lightning サービスコンソールのライセンスをスクラッチ組織に割り当てて、ケースの管理をスピードアップするための Lightning サービスコンソール機能にアクセスできるようにします。
- **[LiveAgent](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_liveagent)**
  Service Cloud でチャットを有効にします。Web ベースチャットを使用して、顧客をエージェントにすばやく接続することでリアルタイムサポートを実現します。
- **[LiveMessage](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_livemessage)**
  Service Cloud でメッセージングを有効にします。メッセージングでは、SMS テキストメッセージや Facebook Messenger などのアプリケーションを使用して、顧客をすばやくサポートします。
- **[LongLayoutSectionTitles](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_longlayoutsectiontitles)**
  ページレイアウトセクションのタイトルに使用できる文字数を最大 80 文字にします。
- **[LoyaltyAnalytics](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltyanalytics)**
  Analytics for Loyalty ライセンスを有効にします。Analytics for Loyalty アプリケーションには、ロイヤルティプログラムについてのアクション可能なインサイトが表示されます。
- **[LoyaltyEngine](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltyengine)**
  Loyalty Management Promotion Setup ライセンスを有効にします。プロモーション設定により、ロイヤルティプログラムマネージャーはロイヤルティプログラムプロセスを作成できます。ロイヤルティプログラムプロセスは、獲得種別と償還種別の受信および新規取引の処理方法を決定するのに役立ちます。
- **[LoyaltyManagementStarter](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymanagementstarter)**
  Loyalty Management - Starter ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。
- **[LoyaltyMaximumPartners:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymaximumpartners)**
  Loyalty Management - Starter ライセンスが有効な組織で、ロイヤルティプログラムに関連付けることができるロイヤルティプログラムパートナーの数を増やします。デフォルトおよび最大値は、1 です。
- **[LoyaltyMaximumPrograms:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymaximumprograms)**
  Loyalty Management - Starter ライセンスが有効な組織で作成できるロイヤルティプログラムの数を増やします。デフォルトおよび最大値は、1 です。
- **[LoyaltyMaxOrderLinePerHour:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymaxorderlineperhour)**
  ロイヤルティプログラムプロセスで 1 時間あたりに累積的に処理できる注文品目の数を増やします。1 ～ 3,500,000 の値を指定します。
- **[LoyaltyMaxProcExecPerHour:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymaxprocexecperhour)**
  ロイヤルティプログラムプロセスで 1 時間あたりに処理できる取引記録の数を増やします。1 ～ 500,000 の値を指定します。
- **[LoyaltyMaxTransactions:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymaxtransactions)**
  処理できる取引記録レコードの数を増やします。1 ～ 50,000,000 の値を指定します。
- **[LoyaltyMaxTrxnJournals:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_loyaltymaxtrxnjournals)**
  Loyalty Management - Start ライセンスが有効な組織に保存できる取引記録レコードの数を増やします。
- **[マクロ](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_macros)**
  スクラッチ組織でマクロを有効にします。マクロを有効にしたら、Lightning コンソールにマクロブラウザーを追加し、よく使用するアクションを実行するための定義済み命令を設定して、複数の投稿に同時に適用できます。
- **[MarketingUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_marketinguser)**
  キャンペーンオブジェクトへのアクセス権を提供します。この設定を行わないと、キャンペーンは参照のみになります。
- **[MaxActiveDPEDefs:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxactivedpedefs)**
  組織で有効化できるデータ処理エンジン定義の数を増やします。1 ～ 50 の値を指定します。
- **[MaxApexCodeSize:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxapexcodesize)**
  テスト以外の未管理 Apex コードのサイズ (MB) を制限します。デフォルト値の 10 よりも大きい値を使用するには、Salesforce カスタマーサポートにお問い合わせください。
- **[MaxAudTypeCriterionPerAud](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxaudtypecriterionperaud)**
  利用者あたりの利用種別条件の使用可能数を制限します。デフォルト値は、10 です。
- **[MaxCustomLabels:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxcustomlabels)**
  カスタム表示ラベルの数 (1,000 単位) を制限します。この制限を 10 に設定すると、スクラッチ組織は 10,000 個のカスタム表示ラベルを持つことができます。1 ～ 15 の値を指定します。
- **[MaxDatasetLinksPerDT:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxdatasetlinksperdt)**
  決定表に関連付けることができるデータセットリンクの数を増やします。1 ～ 3 の値を指定します。
- **[MaxDataSourcesPerDPE:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxdatasourcesperdpe)**
  データ処理エンジン定義に含めることができるソースオブジェクトノードの数を増やします。1 ～ 50 の値を指定します。
- **[MaxDecisionTableAllowed:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxdecisiontableallowed)**
  組織で作成できる決定表のルールの数を増やします。1 ～ 30 の値を指定します。
- **[MaxFavoritesAllowed:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxfavoritesallowed)**
  登録できるお気に入りの数を増やします。お気に入りは、ユーザーが登録する Salesforce ページへのショートカットです。ユーザーは、ヘッダーにある [お気に入り] リストドロップダウンをクリックすることで、自分のお気に入りを表示できます。0 ～ 200 の値を指定します。
- **[MaxFieldsPerNode:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxfieldspernode)**
  データ処理エンジン定義のノードに含めることができる項目の数を増やします。1 ～ 500 の値を指定します。
- **[MaxInputColumnsPerDT:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxinputcolumnsperdt)**
  決定表に含めることができる入力項目の数を増やします。1 ～ 10 の値を指定します。
- **[MaxLoyaltyProcessRules:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxloyaltyprocessrules)**
  組織で作成できるロイヤルティプログラムプロセスルールの数を増やします。1 ～ 20 の値を指定します。
- **[MaxNodesPerDPE:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxnodesperdpe)**
  データ処理エンジン定義に含めることができるノードの数を増やします。1 ～ 500 の値を指定します。
- **[MaxNoOfLexThemesAllowed:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxnooflexthemesallowed)**
  使用できるテーマの数を増やします。テーマを使用することで、色、フォント、画像、サイズなどを設定できます。テーマのリストは、[設定] の [テーマとブランド設定] にあります。0 ～ 300 の値を指定します。
- **[MaxOutputColumnsPerDT:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxoutputcolumnsperdt)**
  決定表に含めることができる出力項目の数を増やします。1 ～ 5 の値を指定します。
- **[MaxSourceObjectPerDSL:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxsourceobjectperdsl)**
  決定表のデータセットリンクで選択できるソースオブジェクトの数を増やします。1 ～ 5 の値を指定します。
- **[MaxStreamingTopics:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxstreamingtopics)**
  24 時間以内に配信され、すべての CometD クライアントで共有される PushTopic イベント通知の最大数を増やします。40 ～ 100 の値を指定します。
- **[MaxUserNavItemsAllowed:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxusernavitemsallowed)**
  ユーザーがナビゲーションバーに追加できるナビゲーション項目の数を増やします。0 ～ 500 の値を指定します。
- **[MaxUserStreamingChannels:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxuserstreamingchannels)**
  ユーザー定義の汎用ストリーミングチャネルの最大数を増やします。20 ～ 1,000 の値を指定します。
- **[MaxWritebacksPerDPE:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_maxwritebacksperdpe)**
  データ処理エンジン定義に含めることができる書き戻しオブジェクトノードの数を増やします。1 ～ 50 の値を指定します。
- **[MedVisDescriptorLimit:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_medvisdescriptorlimit)**
  オブジェクトに適用される共有継承のレコードあたりの共有定義の数を増やします。150 ～ 1,600 の値を指定します。
- **[MinKeyRotationInterval](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_minkeyrotationinterval)**
  暗号化鍵素材の循環間隔を 60 秒に 1 回設定します。この機能を指定しない場合、循環間隔は、検索インデックスの鍵素材では 604,800 秒 (7 日) に 1 回、他のすべての鍵素材では 86,400 秒 (24 時間) に 1 回にデフォルト設定されます。
- **[MobileExtMaxFileSizeMB:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_mobileextmaxfilesizemb)**
  Field Service Mobile 拡張機能のファイルサイズ (MB) を増やします。1 ～ 2,000 の値を指定します。
- **[MobileSecurity](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_mobilesecurity)**
  拡張モバイルセキュリティを有効にします。拡張モバイルセキュリティでは、ポリシーの範囲を制御して、組織のニーズに合わせて調整されたセキュリティソリューションを作成できます。オペレーティングシステムのバージョン、アプリケーションのバージョン、デバイスおよびネットワークのセキュリティに基づいてユーザーアクセスを制限できます。違反の重要度を指定することもできます。
- **[MultiLevelMasterDetail](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_multilevelmasterdetail)**
  1 つのオブジェクト (子、または「従」) と別のオブジェクト (親、または「主」) の間に特殊な親子リレーションを作成できるようにします。
- **[MutualAuthentication](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_mutualauthentication)**
  相互認証の受信要求の検証でクライアント証明書を要求します。
- **[MyTrailhead](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_mytrailhead)**
  スクラッチ組織で myTrailhead イネーブルメントサイトにアクセスできるようにします。
- **[NonprofitCloudCaseManagementUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_nonprofitcloudcasemanagementuser)**
  Salesforce.org の Nonprofit Cloud Case Management 管理パッケージを使用および設定するために必要な権限セットライセンスを提供します。これにより、パッケージをスクラッチ組織にインストールできます。
- **[NumPlatformEvents:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_numplatformevents)**
  1 つの組織で作成できるプラットフォームイベント定義の最大数を増やします。5 ～ 20 の値を指定します。
- **[ObjectLinking](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_objectlinking)**
  ルールを作成して、チャネルインタラクションを、顧客の取引先責任者、リード、個人取引先などのオブジェクトにすばやくリンクします (ベータ)。
- **[OrderManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_ordermanagement)**
  Salesforce Order Management ライセンスを提供します。Order Management (注文管理) は、注文捕捉、履行、納入、支払処理、サービスなど、注文ライフサイクルのすべての側面を処理するための中央ハブです。
- **[OrderSaveLogicEnabled](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_ordersavelogicenabled)**
  注文の新規保存方式のスクラッチ組織サポートを有効にします。OrderSaveLogicEnabled では、注文の新規保存方式のみがサポートされます。スクラッチ組織で注文の旧保存方式と新規保存方式の両方が必要な場合は、OrderSaveBehaviorBoth を使用します。
- **[OrderSaveBehaviorBoth](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_ordersavebehaviorboth)**
  注文の新規保存方式と旧保存方式の両方のスクラッチ組織サポートを有効にします。
- **[OutboundMessageHTTPSession](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_outboundmessagehttpsession)**
  [送信セッション ID] オプションが選択されている送信メッセージ定義で HTTP エンドポイント URL を使用できるようにします。
- **[OutcomeManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_outcome_management)**
  Salesforce の結果管理機能とオブジェクトへのアクセス権をユーザーに付与します。
- **[PardotScFeaturesCampaignInfluence](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_pardotscfeaturescampaigninfluence)**
  Pardot ユーザーに対して追加のキャンペーンインフルエンスモデル、つまり初回接触、最終回接触、均等分布を有効にします。
- **[PersonAccounts](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_personaccounts)**
  スクラッチ組織で個人取引先を有効にします。
- **[PipelineInspection](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_pipelineinspection)**
  パイプラインインスペクションを有効にします。パイプラインインスペクションは、総計値、商談、最近の変更のハイライトを示すパイプラインの統合ビューです。
- **[PlatformCache](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformcache)**
  Enables プラットフォームキャッシュを有効にして、3 MB のキャッシュを割り当てます。Lightning プラットフォームキャッシュレイヤーを使用すると、Salesforce セッションおよび組織データをキャッシュするときのパフォーマンスと信頼性が向上します。
- **[PlatformConnect:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformconnect)**
  Salesforce Connect を有効にして、ユーザーが Salesforce 組織外に保存されているデータを表示、検索、変更できるようにします。1 ～ 5 の値を指定します。
- **[PlatformEncryption](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformencryption)**
  Shield Platform Encryption は、保存されているデータを暗号化します。鍵素材を管理して、項目、ファイル、および他のデータを暗号化できます。
- **[PlatformEventsPerDay:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformeventsperday)**
  24 時間以内に配信され、すべての CometD クライアントで共有される標準量のプラットフォームイベント通知の最大数を増やします。10,000 ～ 50,000 の値を指定します。
- **[ProcessBuilder](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_processbuilder)**
  ビジネスプロセスを自動化できる Salesforce フローツールであるプロセスビルダーを有効にします。
- **[ProductsAndSchedules](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_productsandschedules)**
  スクラッチ組織で商品スケジュールを有効にします。この機能を有効にすると、商品に対してデフォルトの商品スケジュールを作成できるようになります。ユーザーは、商談の個別商品のスケジュールも作成できます。
- **[ProductCatalogManagementAddOn](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_productcatalogmanagementaddon)**
  商品カタログ管理機能とオブジェクトへの参照・更新アクセス権を有効にします。
- **[ProductCatalogManagementViewerAddOn](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_productcatalogmanagementvieweraddon)**
  商品カタログ管理機能とオブジェクトへの参照アクセス権を有効にします。
- **[ProductCatalogManagementPCAddOn](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_productcatalogmanagementpcaddon)**
  スクラッチ組織の Partner Community ユーザーに対して、商品カタログ管理機能とオブジェクトへの参照アクセス権を有効にします。
- **[ProgramManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_programmanagement)**
  すべてのプログラム管理およびケース管理機能とオブジェクトへのアクセスを可能にします。
- **[ProviderFreePlatformCache](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_providerfreeplatformcache)**
  セキュリティレビューに合格した管理パッケージには、3 MB の無料のプラットフォームキャッシュ容量が提供されます。この機能は、プロバイダー無料容量という容量種別で使用でき、Developer Edition 組織で自動的に有効になります。プロバイダー無料容量をプラットフォームキャッシュ区分に割り当て、管理パッケージに追加します。
- **[PublicSectorAccess](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_publicsectoraccess)**
  すべての公共セクターの機能とオブジェクトへのアクセスを有効にします。
- **[PublicSectorApplicationUsageCreditsAddOn](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_applicationusagecredits)**
  価格設定に基づいて、公共セクターアプリケーションの追加利用を有効にします。
- **[PublicSectorSiteTemplate](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_psssitetemplate)**
  公共セクターユーザーに対して、利用可能なテンプレートから Experience Cloud サイトを構築するためのアクセスを許可します。
- **[RecordTypes](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_recordtypes)**
  レコードタイプ機能を有効にします。レコードタイプを使用すると、さまざまなビジネスプロセス、選択リストの値、およびページレイアウトを、さまざまなユーザーに提供できます。
- **[RefreshOnInvalidSession](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_refreshoninvalidsession)**
  ユーザーセッションが無効な場合に Lightning ページの自動更新を有効にします。ただし、ページが新しいトークンを検出すると、そのトークンを設定して更新せずに続行を試みます。
- **[RevSubscriptionManagement](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_revsubscriptionmanagement)**
  サブスクリプション管理を有効にします。サブスクリプション管理は、B2B サブスクリプションおよび 1 回限りの販売に対応した API ファーストの商品 -to- キャッシュソリューションです。
- **[S1ClientComponentCacheSize](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_s1clientcomponentcachesize)**
  組織で Lightning コンポーネントを 5 ページまでキャッシュできるようにします。
- **[SalesCloudEinstein](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_salescloudeinstein)**
  Sales Cloud Einstein 機能と Salesforce Inbox を有効にします。Sales Cloud Einstein は、営業プロセスの各プロセスに AI を適用します。
- **[SalesforceContentUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_salesforcecontentuser)**
  Salesforce コンテンツ機能へのアクセスを有効にします。
- **[SalesforceFeedbackManagementStarter](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_salesforcefeedbackmanagementstarter)**
  Salesforce Feedback Management - Starter 機能を使用するためのライセンスを提供します。
- **[SalesforceIdentityForCommunities](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_salesforceidentityforcommunities)**
  ログインやセルフ登録などの Salesforce Identity コンポーネントをエクスペリエンスビルダーに追加します。この機能は、Aura コンポーネントでは必須です。
- **[SalesUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_salesuser)**
  Sales Cloud 機能のライセンスを提供します。
- **[SAML20SingleLogout](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_saml20singlelogout)**
  SAML 2.0 シングルログアウトを使用できるようにします。
- **[SCIMProtocol](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_scimprotocol)**
  SCIM プロトコルベース API のアクセスサポートを有効にします。
- **[SecurityEventEnabled](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_securityeventenabled)**
  イベントモニタリングでセキュリティイベントへのアクセスを有効にします。
- **[SentimentInsightsFeature](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sentimentinsightsfeature)**
  センチメントインサイトをスクラッチ組織で有効化および使用するために必要なライセンスを提供します。センチメントインサイトを使用すると、顧客のセンチメントを分析して、アクション可能なインサイトを取得してセンチメントを改善できます。
- **[ServiceCatalog](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_servicecatalog)**
  従業員サービスカタログを有効にすると、従業員向けの製品とサービスのカタログを作成できます。また、それらの製品およびサービスの従業員の要求を承認済みの文書化された注文にすることもできます。
- **[ServiceCloud](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_servicecloud)**
  Service Cloud ライセンスをスクラッチ組織に割り当てて、メール、電話、ソーシャルメディア、オンラインコミュニティ、チャット、テキストなど、顧客からの連絡方法を選択できるようにします。
- **[ServiceCloudVoicePartnerTelephony](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_servicecloudvoicepartnertelephony)**
  パートナーテレフォニーを使用する Service Cloud Voice のアドオンライセンスをスクラッチ組織に割り当てると、サポートされているテレフォニープロバイダーと統合する Service Cloud Voice コンタクトセンターを設定できます。1 ～ 50 の値を指定します。
- **[ServiceUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_serviceuser)**
  Service Cloud User ライセンスを 1 件追加して、Service Cloud 機能にアクセスできるようにします。
- **[SessionIdInLogEnabled](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sessionidinlogenabled)**
  Apex デバッグログを有効にして、セッション ID を含めます。無効である場合、デバッグログではセッション ID が「SESSION_ID_REMOVED」に置き換えられます。
- **[SFDOInsightsDataIntegrityUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sfdoinsightsdataintegrityuser)**
  ライセンスを Salesforce.org の Insights Platform Data Integrity 管理パッケージに提供します。これにより、パッケージをスクラッチ組織にインストールできます。
- **[SharedActivities](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sharedactivities)**
  ユーザーが複数取引先責任者を ToDo と行動に関連付けられるようにします。
- **[サイト](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sites)**
  Salesforce サイトを有効にして、Salesforce 組織と直接統合される公開 Web サイトとアプリケーションを作成できるようにします。ユーザーは、ユーザー名とパスワードを使用してログインする必要はありません。
- **[SocialCustomerService](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_socialcustomerservice)**
  ソーシャルカスタマーサービスを有効にし、投稿のデフォルトを設定して、Starter Pack を有効にするか、または Social Studio アカウントにサインインします。
- **[StateAndCountryPicklist](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_stateandcountrypicklist)**
  州選択リストと国/テリトリー選択リストを有効にします。州選択リストや国/テリトリー選択リストを使用すると、都道府県、国、テリトリーのデータをテキスト項目に入力する代わりに、事前定義の標準化されたリストから選択できます。
- **[StreamingAPI](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_streamingapi)**
  ストリーミング API を有効化します。
- **[StreamingEventsPerDay:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_streamingeventsperday)**
  24 時間以内に配信され、すべての CometD クライアントで共有される PushTopic イベント通知の最大数を増やします (API バージョン 36.0 以前)。10,000 ～ 50,000 の値を指定します。
- **[SubPerStreamingChannel:<値>](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_subperstreamingchannel)**
  汎用ストリーミングチャネルでの同時クライアント (登録者) の最大数を増やします (API バージョン 36.0 以前)。20 ～ 4,000 の値を指定します。
- **[SubPerStreamingTopic:](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_subperstreamingtopic)**
  PushTopic ストリーミングチャネルでの同時クライアント (登録者) の最大数を増やします (API バージョン 36.0 以前)。20 ～ 4,000 の値を指定します。
- **[SurveyAdvancedFeatures](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_surveyadvancedfeatures)**
  Salesforce Feedback Management - Growth ライセンスで使用できる機能のライセンスを有効にします。
- **[SustainabilityCloud](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sustainabilitycloud)**
  Sustainability Cloud をインストールして設定するために必要な権限セットライセンスと権限セットを提供します。CRM Analytics と CRM Analytics テンプレートを有効にする、または使用するには、DevelopmentWave スクラッチ組織の機能を含めます。
- **[SustainabilityApp](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_sustainabilityapp)**
  Net Zero Cloud を設定するために必要な権限セットライセンスと権限セットを提供します。Tableau CRM と Tableau CRM テンプレートを有効にする、または使用するには、DevelopmentWave スクラッチ組織の機能を含めます。
- **[TCRMforSustainability](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_tcrmforsustainability)**
  Tableau CRM を有効にして、Net Zero Analytics アプリケーションを管理するために必要なすべての権限を有効にします。ユーザーの Analytics アプリケーションを作成して共有すると、環境会計と財務会計を一致させることができます。
- **[TimelineConditionsLimit](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_timelineconditionslimit)**
  イベント種別あたりのタイムラインレコード表示条件の数を 3 に制限します。
- **[TimelineEventLimit](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_timelineeventlimit)**
  タイムラインに表示するイベント種別の数を 5 に制限します。
- **[TimelineRecordTypeLimit](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_timelinerecordtypelimit)**
  イベント種別あたりの関連オブジェクトレコードタイプの数を 3 に制限します。
- **[TimeSheetTemplateSettings](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_timesheettemplatesettings)**
  タイムシートテンプレートにより、タイムシートを自動的に作成するように設定できます。たとえば、開始日と終了日を設定するテンプレートを作成できます。テンプレートをユーザープロファイルに割り当てることで、適切なユーザーに対してタイムシートが作成されます。
- **[TransactionFinalizers](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_transactionfinalizers)**
  Apex Finalizer を実装して、キュー可能 Apex ジョブに関連付けます。
- **[WaveMaxCurrency](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_wavemaxcurrency)**
  CRM Analytics でサポートされる通貨の最大数を増やします。1 ～ 5 の値を指定します。
- **[WavePlatform](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_waveplatform)**
  Wave プラットフォームライセンスを有効にします。
- **[Workflow](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_workflow)**
  ワークフローを有効にして、標準的な内部の手続きやプロセスを自動化できるようにします。
- **[WorkflowFlowActionFeature](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_workflowflowactionfeature)**
  ワークフローアクションからフローを起動できるようにします。
- **[WorkplaceCommandCenterUser](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_workplacecommandcenteruser)**
  Employee、Crisis、EmployeeCrisisAssessment などのオブジェクトへのアクセスを含め、Workplace Command Center の機能にアクセスできるようにします。
- **[WorkThanksPref](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_workthankspref)**
  Chatter で感謝機能を有効にします。



## AccountInspection

取引先インテリジェンスビューを有効にします。取引先インテリジェンスビューは、取引先の総計値、活動、関連する商談やケースを表示する統合ダッシュボードです。



## AccountingSubledgerGrowthEdition

会計補助台帳拡張機能へのアクセスを可能にする 3 つの権限セットが提供されます。

### 詳細情報

スクラッチ組織定義ファイルには、DataProcessingEngine のスクラッチ組織機能も含める必要があります。[データパイプライン] を有効化する必要があります。スクラッチ組織で [設定] メニューを使用した設定が必要です。Salesforce ヘルプの[「会計補助台帳」](https://help.salesforce.com/s/articleView?id=sfdo.Accounting_Subledger.htm&language=ja)を参照してください。



## AccountingSubledgerStarterEdition

会計補助台帳スターター機能へのアクセスを可能にする 3 つの権限セットが提供されます。

### 詳細情報

スクラッチ組織定義ファイルには、DataProcessingEngine のスクラッチ組織機能も含める必要があります。[データパイプライン] を有効化する必要があります。スクラッチ組織で [設定] メニューを使用した設定が必要です。Salesforce ヘルプの[「会計補助台帳」](https://help.salesforce.com/s/articleView?id=sfdo.Accounting_Subledger.htm&language=ja)を参照してください。



## AccountingSubledgerUser

パッケージのインストール時に会計補助台帳拡張機能への組織のアクセスを有効にします。

### 詳細情報

Accounting Subledger または Accounting Subledger for Industries 管理パッケージをインストールすることが必要です。会計補助台帳パッケージをインストールする場合は、商談オブジェクトも設定します。Salesforce ヘルプの[「会計補助台帳の従来のドキュメント」](https://sfdo-docs.s3.us-west-2.amazonaws.com/Accounting_Subledger_Legacy_Documentation.pdf)を参照してください。



## AddCustomApps:<値>

組織で使用できるカスタムアプリケーションの最大数を増やします。1 ～ 30 の値を指定します。

### サポートされる数量

1 ～ 30、乗数: 1



## AddCustomObjects:<値>

組織で使用できるカスタムオブジェクトの最大数を増やします。1 ～ 30 の値を指定します。

### サポートされる数量

1 ～ 30、乗数: 1



## AddCustomRelationships:<値>

オブジェクトで使用できるカスタムリレーションの最大数を増やします。1 ～ 10 の値を指定します。

### サポートされる数量

1 ～ 10、乗数: 5



## AddCustomTabs:<値>

組織で使用できるカスタムタブの最大数を増やします。1 ～ 30 の値を指定します。

### サポートされる数量

1 ～ 30、乗数: 1



## AddDataComCRMRecordCredit:<値>

スクラッチ組織のユーザーに割り当てられる、レコードをインポートするためのクレジット数を増やします。1 ～ 30 の値を指定します。

### サポートされる数量

1 ～ 30、乗数: 1



## AddInsightsQueryLimit:<値>

CRM Analytics のクエリ結果のサイズを増やします。1 ～ 30 の値を指定します (乗数は 10)。数量を 6 に設定するとクエリ結果が 60 に増加します。

### サポートされる数量

1 ～ 30、乗数: 10



## AdditionalFieldHistory:<値>

履歴を追跡できる項目数をデフォルトの 20 項目から増やします。1 ～ 40 の値を指定します。

### サポートされる数量

1 ～ 40、乗数: 1

### 詳細情報

以前の名前: AddHistoryFieldsPerEntity。



## AdmissionsConnectUser

Admissions Connect コンポーネントを有効化します。このスクラッチ組織の機能パラメーターがない場合、カスタム Admissions Connect コンポーネントは空白でレンダリングされます。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
"{
    ""orgName"": ""Omega - Dev Org"",
    ""edition"": ""Partner Developer"",
    ""hasSampleData"": ""true"",
    ""features"": [""DevelopmentWave"", ""AdmissionsConnectUser"",  ""Communities"", ""OmniStudioDesigner"", ""OmniStudioRuntime""],
    ""settings"": {
        ""lightningExperienceSettings"": {
            ""enableS1DesktopEnabled"": true
        },
        ""chatterSettings"": {
            ""enableChatter"": true
        },
        ""languageSettings"": {
            ""enableTranslationWorkbench"": true
        },
        ""enhancedNotesSettings"": {
            ""enableEnhancedNotes"": true
        },
        ""pathAssistantSettings"": {
            ""pathAssistantEnabled"": true
        },
        ""securitySettings"": {
            ""enableAdminLoginAsAnyUser"":true
        },
        ""userEngagementSettings"": {
            ""enableOrchestrationInSandbox"": true,
            ""enableOrgUserAssistEnabled"": true,
            ""enableShowSalesforceUserAssist"": false
        },
        ""experienceBundleSettings"": {
            ""enableExperienceBundleMetadata"": true
        },
        ""communitiesSettings"": {
            ""enableNetworksEnabled"": true,
            ""enableOotbProfExtUserOpsEnable"": true
        },
        ""mobileSettings"": {
            ""enableS1EncryptedStoragePref2"": false
        }
    }
}"
```

### 詳細情報

次に、スクラッチ組織に Admissions Connect パッケージをインストールします。インストール手順については、Salesforce ヘルプの[「Admission Connect のインストール」](https://help.salesforce.com/s/articleView?id=sfdo.AC_Install.htm&language=ja)を参照してください。



## AdvisorLinkFeature

Student Success Hub コンポーネントを有効化します。このスクラッチ組織の機能パラメーターがない場合、カスタム Student Success Hub コンポーネントは空白でレンダリングされます。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
"{
  "edition": "Partner Developer",
  "features": ["Communities","FeatureParameterLicensing","AdvisorLinkFeature"],
  "orgName": "SAL - Dev Workspace",
  "hasSampleData": "true",
  "settings": {
    "chatterSettings": {
      "enableChatter": true
    },
    "communitiesSettings": {
      "enableNetworksEnabled": true,
      "enableOotbProfExtUserOpsEnable": true
    },
    "enhancedNotesSettings": {
      "enableEnhancedNotes": true
    },
    "experienceBundleSettings": {
      "enableExperienceBundleMetadata": true
    },
    "lightningExperienceSettings": {
      "enableS1DesktopEnabled": true
    },
    "mobileSettings": {
      "enableS1EncryptedStoragePref2": false
    },
    "languageSettings": {
      "enableTranslationWorkbench": true
    },
    "securitySettings": {
        "enableAdminLoginAsAnyUser":true
    }
  }
}"
```

### 詳細情報

次に、スクラッチ組織に Student Success Hub パッケージをインストールします。設定手順については、Salesforce ヘルプの[「Student Success Hub のインストール」](https://help.salesforce.com/s/articleView?id=sfdo.SSH_Install.htm&language=ja)を参照してください。



## AdvisorLinkPathwaysFeature

Pathways コンポーネントを有効化します。このスクラッチ組織の機能パラメーターがない場合、カスタム Pathways コンポーネントは空白でレンダリングされます。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
"{"orgName": "Pathways - Dev Org",
"edition": "Partner Developer",
"features": ["Communities","FeatureParameterLicensing","AdvisorLinkFeature","AdvisorLinkPathwaysFeature"],
"settings": {
"chatterSettings": {
"enableChatter": true
},
"enhancedNotesSettings": {
"enableEnhancedNotes": true
},
"communitiesSettings": {
"enableNetworksEnabled": true
},
"languageSettings": {
"enableTranslationWorkbench": true
},
"lightningExperienceSettings": {
"enableS1DesktopEnabled": true
},
"mobileSettings": {
"enableS1EncryptedStoragePref2": false
}
}
}"
```

### 詳細情報

次に、スクラッチ組織に Pathways パッケージをインストールします。設定手順については、Salesforce ヘルプの[「Pathways の設定」](https://help.salesforce.com/s/articleView?id=sfdo.ssh_setup_pathways.htm&language=ja)を参照してください。



## AIAttribution

Marketing Cloud Account Engagement 用 Einstein 属性へのアクセス権の提供。Einstein 属性は、AI モデリングを使用して、複数のキャンペーンタッチポイントに動的に属性のパーセントを割り当てます。

### サンプルのスクラッチ組織定義ファイル

Einstein 属性を有効にする前に、enableAIAttribution と enableCampaignInfluence2 を true に設定します。

```
{
  "orgName": "NTOutfitters",
  "edition": "Enterprise",
  "features": ["AIAttribution"],
  "settings": {
    "campaignSettings": {
        "enableAIAttribution": true
        "enableCampaignInfluence2": true

    }
}
```

### 詳細情報

この機能は Account Engagement Advanced Edition および Premium Edition で使用できます。

省略可能な設定手順は、スクラッチ組織の [設定] からアクセスできます。詳細は、Salesforce ヘルプの[「Einstein 属性」](https://help.salesforce.com/s/articleView?id=sf.pardot_einstein_attribution_parent.htm&type=5&language=ja)を参照してください。



## AnalyticsAdminPerms

CRM Analytics テンプレートアプリケーションや CRM Analytics アプリケーションの作成を可能にする権限など、CRM Analytics プラットフォームの管理に必要なすべての権限を有効にします。

### 詳細情報

詳細は、Salesforce ヘルプの[「CRM Analytics プラットフォームの設定」](https://help.salesforce.com/articleView?id=bi_help_setup.htm&type=5&language=ja)を参照してください。



## AnalyticsAppEmbedded

CRM Analytics プラットフォーム用の CRM Analytics Embedded App ライセンスを 1 つ提供します。



## API

API アクセス権が提供されないエディション (Professional、Group) であっても、REST API はデフォルトで有効になっています。このスクラッチ組織の機能を使用して、追加の API (SOAP、ストリーミング、Bulk、Bulk 2.0) にアクセスします。

### 詳細情報

詳細は、[「API へのアクセス権を持つ Salesforce エディション」](https://help.salesforce.com/articleView?id=000326486&type=1&mode=1&language=ja)を参照してください。



## ArcGraphCommunity

Experience Cloud ページに Actionable Relationship Center (ARC) コンポーネントを追加することで、ユーザーが ARC リレーショングラフを表示できるようになります。

### 詳細情報

FinancialServicesEALoginAddon アドオンライセンスのシートを 1 つ提供します。

Financial Services Cloud をインストールする必要があります。『Financial Services Cloud システム管理者ガイド』の[「ARC コンポーネントを使用した Experience Cloud テンプレートのカスタマイズ」](https://developer.salesforce.com/docs/atlas.en-us.financial_services_cloud_admin_guide.meta/financial_services_cloud_admin_guide/fsc_admin_arc_experience_cloud.htm)を参照してください。



## 評価

動的評価機能を有効にします。これにより、評価の質問と評価の質問セットの両方が有効になります。

### 詳細情報

これらのオプションは、スクラッチ組織機能定義ファイルに追加します。「エディション」では、サポートされるスクラッチ組織のいずれかの機能エディションを指定できます。

```
{
  "orgName": "Sample Org",
  "edition": "Developer",
  "features": ["Assessments"],
  "settings": {
    "industriesSettings": {
      "enableIndustriesAssessment": true,
      "enableDiscoveryFrameworkMetadata": true
    }
  }
}
```

調査をページレイアウトに追加します。詳細は Salesforce ヘルプの[「ページレイアウト」](https://help.salesforce.com/s/articleView?id=sf.customize_layout.htm&type=5&language=ja)を参照してください。



## AssetScheduling:<value>

Asset Scheduling ライセンスを有効にします。アセットのスケジュールにより、部屋と機器を簡単に予約できます。1 ～ 10 の値を指定します。

### サポートされる数量

1 ～ 10

### 詳細情報

詳細は、Salesforce ヘルプの[「Salesforce Scheduler でのアセットのスケジュールの有効化」](https://help.salesforce.com/articleView?id=ls_overview.htm&type=5;&language=ja)を参照してください。



## AssociationEngine

関連付けエンジンを有効化します。これにより支店ユニット顧客レコードを作成することで、新しい取引先がユーザーの現在の支店に自動的に関連付けられます。

### 詳細情報

FSCComprehensivePsl ユーザーライセンスを 11 シートと、FSCComprehensiveAddOn アドオンライセンスを 11 シートを提供します。

Financial Services Cloud をインストールする必要があります。『メタデータ API 開発者ガイド』の[「AssociationEngineSettings」](https://developer.salesforce.com/docs/atlas.ja-jp.api_meta.meta/api_meta/meta_associationenginesettings.htm)を参照してください。



## AuthorApex

スクラッチ組織で Apex コードにアクセスして変更できるようにします。Enterprise Edition と Developer Edition ではデフォルトで有効になっています。

### 詳細情報

Group Edition 組織と Professional Edition 組織の場合、この機能はデフォルトで無効になっています。AuthorApex 機能を有効にすると、Apex クラスを編集およびテストできます。



## B2BCommerce

B2B ライセンスを提供します。B2BCommerce により、組織で企業間 (B2B) 取引が可能になります。B2B ストアを作成および更新します。バイヤーアカウントを作成および管理します。商品を他の企業に販売します。

### 詳細情報

B2B Commerce を使用してストアを作成するためには、スクラッチ組織定義ファイルにコミュニティのスクラッチ組織機能も含める必要があります。Professional Edition、Partner Professional Edition、Group Edition、および Partner Group Edition 組織では使用できません。



## B2BLoyaltyManagement

B2B Loyalty Management ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。

### 詳細情報

詳細は、Salesforce ヘルプの[「ロイヤルティ管理」](https://help.salesforce.com/s/articleView?id=sf.loyaltyoverview.htm&language=ja)を参照してください。



## B2CCommerceGMV

B2B2C Commerce ライセンスを提供します。B2B2C Commerce では、e コマースサイトを迅速に立ち上げ、複数のデジタルチャネルでブランドのプロモーションや製品の販売を行うことができます。組織の小売ストアフロントの作成や更新、個人取引先の作成や管理が可能です。

### 詳細情報

スクラッチ組織定義ファイルにコミュニティ機能を指定する必要もあります。

Professional Edition、Partner Professional Edition、Group Edition、および Partner Group Edition 組織では使用できません。

詳細は、Salesforce ヘルプの[「Salesforce B2B Commerce および B2B2C Commerce」](https://help.salesforce.com/s/articleView?id=sf.comm_intro.htm&language=ja)を参照してください。



## B2CLoyaltyManagement

Loyalty Management - Growth ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。

### 詳細情報

詳細は、Salesforce ヘルプの[「ロイヤルティ管理」](https://help.salesforce.com/s/articleView?id=sf.loyaltyoverview.htm&language=ja)を参照してください。



## B2CLoyaltyManagementPlus

Loyalty Management - Advanced ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。

### 詳細情報

詳細は、Salesforce ヘルプの[「ロイヤルティ管理」](https://help.salesforce.com/s/articleView?id=sf.loyaltyoverview.htm&language=ja)を参照してください。



## BatchManagement

Batch Management ライセンスを有効にします。一括管理により、管理しやすいバッチで大量のレコードを処理できます。

### 詳細情報

詳細は、Salesforce ヘルプの[「一括管理」](https://help.salesforce.com/s/articleView?id=sf.concept_batch_management.htm&language=ja)を参照してください。



## BigObjectsBulkAPI

スクラッチ組織が Bulk API で BigObjects を使用できるようにします。

### 詳細情報

詳細は[『Big Object Implementation Guide (Big Object 実装ガイド)』](https://developer.salesforce.com/docs/atlas.en-us.bigobjects.meta/bigobjects/big_object.htm)を参照してください。



## ブリーフケース

スクラッチ組織でブリーフケースビルダーを使用できるようにします。これにより、オフラインブリーフケースを作成し、選択したレコードをオフラインで表示できるようになります。



## BudgetManagement

予算管理機能とオブジェクトへのアクセス権をユーザーに付与します。予算管理機能を有効にするには、この機能をスクラッチ組織定義ファイルに追加します。

### 詳細情報

詳細は、Salesforce ヘルプの[「予算管理」](https://help.salesforce.com/s/articleView?id=sf.grmk_budget_management_for_grantmaking.htm&language=ja)を参照してください。



## BusinessRulesEngine

ビジネスルールエンジンを有効化します。これにより、式セットとルックアップテーブルの両方が有効化されます。

### 詳細情報

ビジネスルールエンジンデザイナーとビジネスルールエンジンランタイムのライセンスをそれぞれ 10 個提供します。詳細は、Salesforce ヘルプの[「ビジネスルールエンジン」](https://help.salesforce.com/s/articleView?id=sf.business_rules_engine.htm&type=5&language=ja)を参照してください。



## CacheOnlyKeys

キャッシュのみの鍵サービスを有効にします。この機能では、Salesforce 外部の鍵素材を保存したり、キャッシュのみの鍵サービスを使用して、制御する鍵サービスからオンデマンドで鍵を取得したりできます。

### 詳細情報

スクラッチ組織で [設定] メニューを使用して、[PlatformEncryption](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformencryption) および設定を有効にする必要があります。Salesforce ヘルプの[「Shield Platform Encryption に必要なユーザー権限」](https://help.salesforce.com/articleView?id=security_pe_permissions.htm&language=ja)、[「Salesforce を使用したテナントの秘密の生成」](https://help.salesforce.com/articleView?id=security_pe_ui_setup.htm&language=ja)、[「キャッシュのみの鍵サービス」](https://help.salesforce.com/articleView?id=security_pe_byok_cache.htm&type=5&language=ja)を参照してください。



## CalloutSizeMB:<値>

Apex コールアウトの最大サイズを増やします。3 ～ 12 の値を指定します。

### サポートされる数量

3 ～ 12、乗数: 1



## CampaignInfluence2

Sales Cloud と Marketing Cloud Account Engagement でのカスタマイズ可能なキャンペーンインフルエンスへのアクセスを提供します。カスタマイズ可能なキャンペーンインフルエンスでは、属性を追跡するために、キャンペーンと商談間のリレーションを自動的に関連付けたり、手動で作成したりできます。

### サンプルのスクラッチ組織定義ファイル

カスタマイズ可能なキャンペーンインフルエンスを有効化するには、enableCampaignInfluence2 を true に設定します。

```
{
  "orgName": "NTOutfitters",
  "edition": "Enterprise",
  "features": ["CampaignInfluence2"],
  "settings": {
    "campaignSettings": {
        "enableCampaignInfluence2": true

    }
}
```

### 詳細情報

この機能は、Salesforce Enterprise Edition、Performance Edition、Unlimited Edition、Developer Edition で使用できます。

省略可能な設定手順は、スクラッチ組織の [設定] からアクセスできます。詳細は、Salesforce ヘルプの[「カスタマイズ可能なキャンペーンインフルエンス」](https://help.salesforce.com/s/articleView?id=sf.campaigns_influence_customizable.htm&type=5&language=ja)を参照してください。



## CascadeDelete

以前は主従関係でのみ使用できたカスケード削除機能を、ルックアップリレーションでも使用できるようにします。レコードが誤って削除されないようにするため、デフォルトではカスケード削除は無効になっています。



## CaseClassification

Einstein ケース分類を有効にします。ケース分類は、エージェントが最適な値を選択できるように、おすすめを提供します。また、自動的に最適なおすすめを保存して、ケースを適切なエージェントにルーティングすることもできます。



## CaseWrapUp

Einstein ケースラップアップを有効にします。エージェントがすばやくケースを完了できるように、Einstein ケースラップアップが過去のチャットトランスクリプトに基づいてケース項目値を推奨します。

### 詳細情報

Enterprise Edition スクラッチ組織で使用できます。

スクラッチ組織で [設定] メニューを使用した設定が必要です。

詳細は、Salesforce ヘルプの[「Einstein 分類アプリケーションの設定」](https://help.salesforce.com/articleView?id=cc_service_what_is.htm&language=ja)を参照してください。



## ChangeDataCapture

スクラッチ組織のエディションで変更データキャプチャが自動的に有効にならない場合に、変更データキャプチャを有効にします。



## Chatbot

ボットメタデータをスクラッチ組織にリリースして、ボットを作成および編集できるようにします。

### 詳細情報

この機能を使用するには、Dev Hub 組織で **[Einstein 機能を有効化]** をオンにしてサービスの利用規約に同意します。

詳細は Salesforce ヘルプの[「Einstein ボット」を](https://help.salesforce.com/articleView?id=bots_service_intro.htm&type=5&language=ja)参照してください。



## ChatterEmailFooterLogo

ChatterEmailFooterLogo により、ロゴ画像のドキュメント ID を使用して Chatter メールをカスタマイズできます。

### 詳細情報

詳細は Salesforce ヘルプの[「メール通知へのカスタムブランドの追加」](https://help.salesforce.com/s/articleView?id=sf.collab_admin_email_customize.htm&type=5&language=ja)を参照してください。



## ChatterEmailFooterText

ChatterEmailFooterText により、カスタム Chatter メールでフッターテキストを使用できるようになります。

### 詳細情報

詳細は Salesforce ヘルプの[「メール通知へのカスタムブランドの追加」](https://help.salesforce.com/s/articleView?id=sf.collab_admin_email_customize.htm&type=5&language=ja)を参照してください。



## ChatterEmailSenderName

ChatterEmailSenderName により、メール通知の送信者名として表示される名前をカスタマイズできます。たとえば、会社の名前を指定できます。

### 詳細情報

詳細は Salesforce ヘルプの[「Chatter のメール設定とブランド設定」](https://help.salesforce.com/s/articleView?id=sf.collab_admin_email_settings.htm&type=5&language=ja)を参照してください。



## CloneApplication

CloneApplication により、既存のカスタム Lightning アプリケーションをコピーして、その新しいアプリケーションで必要なカスタマイズを行うことができます。この方法によってゼロから始める必要がなくなり、特に簡単なバリエーションのアプリケーションを作成するときに役立ちます。

### 詳細情報

詳細は、Salesforce ヘルプの[「Lightning アプリケーションの作成」](https://help.salesforce.com/s/articleView?id=sf.apps_lightning_create.htm.htm&language=ja)を参照してください。



## CMSMaxContType

Salesforce CMS で作成できる個別のコンテンツ種別の数を 21 に制限します。



## CMSMaxNodesPerContType

特定のコンテンツ種別に対して作成できる子ノード (項目) の最大数を 15 に制限します。



## CMSUnlimitedUse

Salesforce CMS でのコンテンツレコード数、コンテンツ種別数、帯域幅の使用を無制限にします。



## コミュニティ

組織でカスタマーコミュニティを作成できるようにします。コミュニティを使用するには、スクラッチ組織定義ファイルの設定セクションに [communitiesSettings] > [enableNetworksEnabled] を含める必要もあります。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。



## ConAppPluginExecuteAsUser

ConnectedApp メタデータ API オブジェクトで pluginExecutionUser 項目を有効にします。



## ConcStreamingClients:<値>

API バージョン 36.0 以前のすべてのチャネルとすべてのイベント種別での、同時クライアント (登録者) の最大数を増やします。20 ～ 4,000 の値を指定します。

### サポートされる数量

20 ～ 4,000、乗数: 1



## ConnectedAppCustomNotifSubscription

接続アプリケーションを有効化して、カスタムデスクトップおよびモバイルの通知を送信するために使用するカスタム通知種別を登録できるようにします。

### 詳細情報

カスタム通知を送信するには、通知タイプを作成する [CustomNotificationType](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_customnotificationtype) と、通知タイプを登録する ConnectedAppCustomNotifSubscription の両方が必要です。カスタム通知の詳細は、Salesforce ヘルプの[「通知ビルダーを使用した通知の管理」](https://help.salesforce.com/s/articleView?id=sf.notif_builder.htm&language=ja)を参照してください。



## ConnectedAppToolingAPI

Tooling API で接続アプリケーションを使用できるようにします。



## ConsentEventStream

組織で「Consent Event Stream (同意イベントストリーム)」権限を有効にします。

### 詳細情報

詳細は、Salesforce ヘルプの[「同意イベントストリームの使用」](https://help.salesforce.com/s/articleView?id=sf.consent_event_stream.htm&type=5&language=ja)を参照してください。



## ConsolePersistenceInterval:<値>

コンソールデータを保存する頻度を分単位で増やします。0 ～ 500 の値を指定します。自動保存を無効にするには値を 0 に設定します。

### サポートされる数量

0 ～ 500、乗数: 1



## ContactsToMultipleAccounts

取引先責任者-to-複数取引先機能を有効化します。この機能により、1 人の取引先責任者を複数の取引先に関連付けることができます。



## ContractApprovals

取引先責任者の承認を有効化して、承認プロセスを通して契約を追跡できるようにします。



## ContractManagement

組織で契約ライフサイクル管理 (CLM) 機能を有効にします。



## ContractMgmtInd

業種の契約ライフサイクル管理 (CLM) 機能を有効にします。



## CPQ

Salesforce CPQ 管理パッケージのインストールに必要なライセンス機能が有効化されますが、パッケージは自動的にインストールされません。

### 詳細情報

設定手順の詳細は、Salesforce ヘルプの[「CPQ を使用した見積の管理」](https://help.salesforce.com/articleView?id=cpq_master.htm&type=5&language=ja)を参照してください。



## CustomFieldDataTranslation

ユーザーが作業種別グループオブジェクト、サービステリトリーオブジェクト、サービスリソースオブジェクトのカスタム項目データの翻訳を可能にします。テキスト型、テキストエリア型、ロングテキストエリア型、テキストエリア (リッチ) 型、および URL 型のカスタム項目のデータ翻訳を有効にできます。

### 詳細情報

スクラッチ組織定義ファイルには、EntityTranslation のスクラッチ組織機能も含める必要があります。Professional Edition、Partner Professional Edition、Group Edition、および Partner Group Edition 組織では使用できません。



## CustomNotificationType

カスタムデスクトップおよびモバイル通知を送信するために使用するカスタム通知タイプを組織で作成できるようにします。

### 詳細情報

カスタム通知を送信するには、通知タイプを作成する CustomNotificationType と、通知タイプを登録する [ConnectedAppCustomNotifSubscription](https://developer.salesforce.com/docs/atlas.ja-jp.252.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_connectedappcustomnotifsubscription) の両方が必要です。カスタム通知の詳細は、Salesforce ヘルプの[「通知ビルダーを使用した通知の管理」](https://help.salesforce.com/s/articleView?id=sf.notif_builder.htm&language=ja)を参照してください。



## DataComDnbAccounts

Data.com 取引先機能のライセンスを提供します。



## DataComFullClean

Data.com クリーニング機能のライセンスを提供し、ジョブの自動入力クリーンアップ設定を有効にします。



## DataMaskUser

30 件の Data Mask 権限セットライセンスを提供します。この権限セットにより、インストールされている Salesforce Data Mask パッケージにアクセスできるようになります。

### 詳細情報

インストールと設定の手順については、Salesforce ヘルプの[「管理パッケージのインストール」](https://help.salesforce.com/articleView?id=data_mask_install.htm&type=5&language=ja)を参照してください。



## DataProcessingEngine

Data Processing Engine ライセンスを有効にします。データ処理エンジンでは、Salesforce 組織で使用可能なデータを変換し、その結果を新規レコードまたは更新レコードとして書き戻すことができます。

### 詳細情報

詳細は、Salesforce ヘルプの[「データ処理エンジン」](https://help.salesforce.com/s/articleView?id=sf.concept_data_processing_engine.htm&language=ja)を参照してください。



## DebugApex

Apex 対話型デバッガーを有効にします。このデバッガーを使用すると、ブレークポイントとチェックポイントを設定して Apex コードをデバッグし、コードからバグを見つけることができます。



## DecisionTable

Decision Table ライセンスを有効にします。決定表はビジネスルールを読み取り、Salesforce 組織内のレコードまたは指定した値の結果を決定します。

### 詳細情報

詳細は、Salesforce ヘルプの[「決定表」](https://help.salesforce.com/s/articleView?id=concept_decision_table.htm&language=ja)を参照してください。



## DefaultWorkflowUser

スクラッチ組織の管理者をデフォルトのワークフローユーザーとして設定します。



## DeferSharingCalc

グループメンバーシップとルール計算の共有を一時的に停止して、後で再開できるようにします。

### 詳細情報

スクラッチ組織で [設定] メニューを使用した設定が必要です。Salesforce ヘルプの[「共有適用の延期」](https://help.salesforce.com/articleView?id=security_sharing_defer_sharing_calculations.htm&type=5&language=ja)を参照してください。



## DevelopmentWave

スクラッチ組織で CRM Analytics 開発を有効にします。5 件のプラットフォームライセンスと 5 件の CRM Analytics プラットフォームライセンスを組織に割り当て、権限セットライセンスを管理ユーザーに割り当てます。CRM Analytics テンプレートと Einstein Discovery 機能も有効にします。



## DeviceTrackingEnabled

デバイス追跡を有効にします。



## DevOpsCenter

スクラッチ組織の DevOps センターを有効にします。これにより、パートナーは、DevOps センターアプリケーション (基本) パッケージの機能を拡張、強化する第二世代管理パッケージを作成できるようになります。

### Dev Hub 組織

DevOps センターを Dev Hub 組織で有効にするには Salesforce システム管理者に依頼してください。[設定] から [クイック検索] ボックスに「DevOps センター」と入力し、**[DevOps センター]** を選択します。スクラッチ組織は、組織設定が有効化された後に作成できます。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
{
    "orgName": "Acme",
    "edition": "Enterprise",
    "features": ["DevOpsCenter"],
    "settings": {
        "devHubSettings": {
            "enableDevOpsCenterGA": true
            }  
        }  
    }
```

### 組織シェイプから作成されたスクラッチ組織のスクラッチ組織定義ファイル

組織シェイプに基づいて DevOps センターが有効なスクラッチ組織を作成した場合でも、DevOps センターの契約条件に含まれる法的な理由のため、DevOps センターの機能と設定をスクラッチ組織定義に追加する必要があります。

```
{
    "orgName": "Acme",
    "sourceOrg": "00DB1230400Ifx5",
    "features": ["DevOpsCenter"],
    "settings": {
        "devHubSettings": {
            "enableDevOpsCenterGA": true
            }  
        }  
    }
```

### 詳細情報

Salesforce ヘルプ: [DevOps Center の拡張パッケージを構築する](https://help.salesforce.com/s/articleView?id=sf.devops_center_partners_extension_packages.htm&language=ja)



## DisableManageIdConfAPI

LoginIP オブジェクトと ClientBrowser API オブジェクトへのアクセスを制限して、表示と削除のみを可能にします。



## DisclosureFramework

開示とコンプライアンスのハブの設定に必要な権限セットライセンスと権限セットを提供します。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
{
  "orgName": "dch org",
  "edition": "Developer",
  "features": ["DisclosureFramework"],
  "settings": {
    "industriesSettings":{
      "enableGnrcDisclsFrmwrk": true,
      "enableIndustriesAssessment" : true
    }
  }
}
```

### 詳細情報

設定の手順については、Salesforce ヘルプの「Net Zero Cloud の設定および管理」ガイドの[「開示とコンプライアンスのハブ」](https://help.salesforce.com/s/articleView?id=sf.netzero_setup_disclosure_and_compliance_hub.htm&language=ja)を参照してください。



## Division

[会社の設定] の [ディビジョンの管理] を有効にします。ディビジョンでは、組織のデータを論理セクションに分類できます。これにより、検索、レポート、およびリストビューがユーザーにとってより有用となります。ディビジョンは、データ量が極めて多い組織に有用です。



## DocGen

組織でドキュメント生成機能を有効にします。



## DocGenDesigner

ドキュメントテンプレートの作成および定義を行うためのデザイナーを有効にします。



## DocGenInd

組織で業種のドキュメント生成機能を有効にします。



## DocumentChecklist

ドキュメントの追跡と承認機能を有効にして、「ドキュメントチェックリスト」権限セットを追加します。ドキュメント追跡機能により、アップロードして承認するドキュメントを定義して、ローン申請などのプロセスやアクションプランをサポートできます。

### 詳細情報

詳細は、『Financial Services Cloud システム管理者ガイド』の[「ドキュメントの追跡と承認の有効化」](https://developer.salesforce.com/docs/atlas.en-us.financial_services_cloud_admin_guide.meta/financial_services_cloud_admin_guide/admin_enable_doc_mgmt.htm)を参照してください。



## DocumentReaderPageLimit

データ抽出のために送信されるページ数を 5 に制限します。

### 詳細情報

詳細は、Salesforce ヘルプの[「インテリジェントフォームリーダー」](https://help.salesforce.com/s/articleView?id=sf.form_reader.htm&language=ja)を参照してください。



## DSARPortability

組織でのプライバシーセンターの DSARPortability 機能へのアクセスを有効にします。また、PrivacyCenter ライセンスと PrivacyCenterAddOn ライセンスのシートがそれぞれ 1 個提供されます。

### 詳細情報

詳細は、『Salesforce REST API 開発者ガイド』の[「Portability」](https://developer.salesforce.com/docs/atlas.ja-jp.242.0.api_rest.meta/api_rest/resources_portability.htm)を参照してください。



## DurableClassicStreamingAPI

API バージョン 37.0 以降のデュラブル PushTopic ストリーミング API を有効にします。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。



## DurableGenericStreamingAPI

API バージョン 37.0 以降のデュラブル汎用ストリーミング API を有効にします。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。



## DynamicClientCreationLimit

組織で動的クライアント登録エンドポイントを使用して最大 100 件の OAuth 2.0 接続アプリケーションを登録できるようにします。



## EAndUDigitalSales

組織でエネルギーおよび公益事業のデジタルセールス機能を有効にします。



## EAndUSelfServicePortal

組織で、デジタルエクスペリエンスユーザーのセルフサービスポータル機能を有効にします。



## EAOutputConnectors

CRM Analytics 出力コネクタを有効化します。

### 詳細情報

このスクラッチ組織では、Dev Hub に EAOutputConnectors 権限が必要です。詳細は Salesforce ヘルプの[「Salesforce 出力接続」](https://help.salesforce.com/s/articleView?id=sf.bi_integrate_connectors_output_salesforce.htm&language=ja)を参照してください。



## EASyncOut

CRM Analytics SyncOut を有効にします。

### 詳細情報

このスクラッチ組織では、Dev Hub に EASyncOut 権限が必要です。詳細は、Salesforce ヘルプの[「Sync Out for Snowflake」](https://help.salesforce.com/s/articleView?id=sf.bi_integrate_connectors_sync_out_snowflake.htm&language=ja)を参照してください。



## EdPredictionM3Threshold

ペイロードのレコード数を 10 に設定します。それ以降、Einstein Discovery 予測サービスは M3 を使用します。



## EdPredictionTimeout

1 つの Einstein Discovery 予測の最大継続時間を 100 ミリ秒に設定します。



## EdPredictionTimeoutBulk

Einstein Discovery 予測を一括で実行する際の 1 つの Einstein Discovery 予測の最大継続時間を 10 ミリ秒に設定します。



## EdPredictionTimeoutByomBulk

Bring Your Own Model (BYOM) の 1 つの Einstein Discovery 予測の最大継続時間を 100 ミリ秒に設定します。



## EducationCloud: <value>

Education Cloud を使用できるようにします。

### サポートされる数量

最大: 10、乗数: 1

### 詳細情報

この機能を有効にした後に、標準の設定手順を行う必要があります。詳細は、Salesforce ヘルプの[「Education Cloud の設定」](https://help.salesforce.com/s/articleView?id=sfdo.EC_Set_Up_Education_Cloud.htm&language=ja)を参照してください。



## EinsteinAnalyticsPlus

CRM Analytics プラットフォーム用の CRM Analytics Plus ライセンスを 1 つ提供します。



## EinsteinArticleRecommendations

Einstein 記事のおすすめのライセンスを提供します。Einstein 記事のおすすめでは、過去のケースのデータを使用して、カスタマーサービスエージェントが顧客からの問い合わせに対応するのに最も役立ちそうなナレッジ記事を識別します。

### 詳細情報

Enterprise Edition スクラッチ組織で使用できます。

スクラッチ組織で [設定] メニューを使用した設定が必要です。

詳細は Salesforce ヘルプの[「Einstein 記事のおすすめの設定」](https://help.salesforce.com/articleView?id=einstein_article_recommendations_set_up.htm&type=5&language=ja)を参照してください。



## EinsteinBuilderFree

システム管理者が Einstein 予測ビルダーで 1 件の有効な予測を作成できるようにするライセンスを提供します。Einstein 予測ビルダーは、システム管理者向けのカスタム AI です。

### 詳細情報

設定の手順については、Salesforce ヘルプの[「Einstein 予測ビルダー」](https://help.salesforce.com/articleView?id=custom_ai_prediction_builder.htm&type=0&language=ja)を参照してください。



## EinsteinDocReader

インテリジェントフォームリーダーをスクラッチ組織で有効化および使用するために必要なライセンスを提供します。インテリジェントフォームリーダーは光学式文字認識と Amazon Textract を使用してデータを自動に抽出します。

### 詳細情報

このスクラッチ組織機能を使用するには、Dev Hub 組織に EinsteinDocReader および SalesforceManagedIFR 権限が必要です。インテリジェントフォームリーダーについては、Salesforce ヘルプの[「インテリジェントフォームリーダー」](https://help.salesforce.com/s/articleView?id=sf.form_reader.htm&language=ja)を参照してください。



## EinsteinRecommendationBuilder

Einstein レコメンデーションビルダーでおすすめを作成するためのライセンスを提供します。Einstein レコメンデーションビルダーではカスタム AI レコメンデーションを構築できます。

### 詳細情報

Developer Edition および Enterprise Edition で有効になっています。

スクラッチ組織で [設定] メニューを使用した設定が必要です。また、スクラッチ組織で Einstein レコメンデーションビルダーを使用するためには、EinsteinRecommendationBuilderMetadata 機能が必要です。

詳細は、Salesforce ヘルプの[「Einstein レコメンデーションビルダー」](https://help.salesforce.com/apex/HTViewHelpDoc?id=custom_ai_recommendation_builder.htm&language=ja)を参照してください。



## EinsteinRecommendationBuilderMetadata

Einstein レコメンデーションビルダーが必要なメタデータ API を使用できるようにします。この機能を有効にすると、カスタム AI レコメンデーションを構築できます。

### 詳細情報

Developer Edition および Enterprise Edition で有効になっています。

スクラッチ組織で [設定] メニューを使用した設定が必要です。また、スクラッチ組織で Einstein レコメンデーションビルダーを使用するためには、EinsteinRecommendationBuilderMetadata 機能が必要です。

詳細は、Salesforce ヘルプの[「Einstein レコメンデーションビルダー」](https://help.salesforce.com/apex/HTViewHelpDoc?id=custom_ai_recommendation_builder.htm&language=ja)を参照してください。



## EinsteinSearch

スクラッチ組織で Einstein Search 機能を使用および有効化するために必要なライセンスを提供します。

### 詳細情報

Professional および Enterprise Edition のスクラッチ組織で使用できます。

スクラッチ組織で [設定] メニューを使用した設定が必要です。

詳細は、Salesforce ヘルプの[「Einstein 検索設定の管理」](https://help.salesforce.com/apex/HTViewHelpDoc?id=search_es_settings.htm&language=ja)を参照してください。



## EinsteinVisits

Consumer Goods Cloud を有効にします。Consumer Goods Cloud を使用すると、小売チャネルパートナーとのコラボレーション方法が変わります。営業マネージャーは、訪問を計画し、店舗をまたがってビジネスの健全性を分析できます。また、フィールド営業担当者は、リテールエグゼキューションモバイルアプリケーションを使用して在庫を追跡し、注文を受け付け、訪問の詳細を記録できます。



## EinsteinVisitsED

Einstein Discovery を有効化します。Einstein Discovery は、店舗訪問レコメンデーションを取得する場合に使用します。Einstein 訪問 ED を使用すると訪問頻度戦略を作成することができ、これにより Einstein は、最適な店舗訪問レコメンデーションを提供できます。

### 詳細情報

Salesforce ヘルプの[「訪問頻度の Next Best Action 戦略の作成」](https://help.salesforce.com/s/articleView?id=sf.industries_einstein_visit_frequency_strategy.htm&type=5&language=ja)を参照してください。



## EmbeddedLoginForIE

IE11 で組み込みログインをサポートする JavaScript ファイルを提供します。



## EmpPublishRateLimit:<値>

毎時公開される標準量のプラットフォームイベント通知の最大数を増やします。1,000 ～ 10,000 の値を指定します。

### サポートされる数量

1,000 ～ 10,000、乗数: 1



## EnablePRM

組織でパートナーリレーション管理権限を有効にします。



## EnableManageIdConfUI

LoginIP オブジェクトと ClientBrowser API オブジェクトにアクセスして、UI でユーザーの ID を検証できるようにします。



## EnableSetPasswordInApi

sf org generate password を使用して、古いパスワードを入力せずにパスワードを変更できるようにします。



## EncryptionStatisticsInterval:<value>

暗号化統計収集プロセスの間隔 (秒単位) を定義します。最大値は 604,800 秒 (7 日) です。デフォルトは 86,400 秒 (24 時間) に 1 回です。

### サポートされる数量

0 ～ 60,4800、乗数: 1

### 詳細情報

スクラッチ組織で [設定] メニューを使用して、[PlatformEncryption](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformencryption) およびいくつかの設定を有効にする必要があります。Salesforce ヘルプの[「Shield Platform Encryption に必要なユーザー権限」](https://help.salesforce.com/articleView?id=security_pe_permissions.htm&language=ja)と[「Salesforce を使用したテナントの秘密の生成」](https://help.salesforce.com/articleView?id=security_pe_ui_setup.htm&language=ja)を参照してください。



## EncryptionSyncInterval:<value>

組織がデータを有効な鍵素材と同期できる頻度 (秒単位) を定義します。デフォルト値は、最大値の 604,800 秒 (7 日) です。データの同期頻度を高めるには、0 以上の秒単位の値を指定します。

### サポートされる数量

0 ～ 604,800、乗数: 1

### 詳細情報

スクラッチ組織で [設定] メニューを使用して、[PlatformEncryption](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformencryption) およびいくつかの設定を有効にする必要があります。Salesforce ヘルプの[「Shield Platform Encryption に必要なユーザー権限」](https://help.salesforce.com/articleView?id=security_pe_permissions.htm&language=ja)と[「Salesforce を使用したテナントの秘密の生成」](https://help.salesforce.com/articleView?id=security_pe_ui_setup.htm&language=ja)を参照してください。



## EnergyAndUtilitiesCloud

組織で、Energy and Utilities Cloud 機能を有効にします。



## エンタイトルメント

エンタイトルメントの有効化。エンタイトルメントは、サービス契約の利用規約を表す Salesforce のカスタマーサポートのユニット (「電話サポート」や「Web サポート」など) です。



## EventLogFile

組織のイベントログファイルへの API アクセスを有効にします。イベントモニタリング製品では、Salesforce 組織の操作イベントに関する情報を収集します。この情報を使用して、利用状況のトレンドやユーザーの操作を分析できます。



## EntityTranslation

ユーザーが作業種別グループオブジェクト、サービステリトリーオブジェクト、サービスリソースオブジェクトの項目データの翻訳を可能にします。

### 詳細情報

カスタム項目データを翻訳するには、スクラッチ組織定義ファイルには、CustomFieldDataTranslation のスクラッチ組織機能も含める必要があります。Professional Edition、Partner Professional Edition、Group Edition、および Partner Group Edition 組織では使用できません。



## ExpressionSetMaxExecPerHour

Connect REST API を使用することで、組織では 1 時間あたり最大 50 万の式セットを実行できるようになります。

詳細は、Salesforce 開発者ドキュメントの[「式セット」](https://developer.salesforce.com/docs/atlas.en-us.industries_reference.meta/industries_reference/connect_resources_bre_expression_set.htm)を参照してください。



## ExternalIdentityLogin

スクラッチ組織で外部 ID ライセンスに関連付けられている Salesforce Customer Identity 機能を使用できるようにします。



## FieldAuditTrail

組織で項目監査履歴を有効にして、60 件までの項目を追跡できるようにします。デフォルトでは 20 件の項目がすべての組織で追跡され、項目監査履歴ではさらに 40 件の項目が追跡されます。

### 詳細情報

以前の名前: RetainFieldHistory



## FieldService:<value>

Field Service ライセンスを提供します。1 ～ 25 の値を指定します。

### サポートされる数量

1 ～ 25、乗数: 1

### 詳細情報

Enterprise Edition で使用できます。Developer Edition では、デフォルトで有効になっています。詳細は、Salesforce ヘルプの[「Field Service の有効化」](https://help.salesforce.com/articleView?id=fs_enable.htm&language=ja)を参照してください。



## FieldServiceAppointmentAssistantUser:<value>

Field Service 予定アシスタントの権限セットライセンスを追加します。1 ～ 25 の値を指定します。

### サポートされる数量

1 ～ 25、乗数: 1

### 詳細情報

詳細は、Salesforce ヘルプの[「Field Service 予定アシスタントの設定」](https://help.salesforce.com/s/articleView?language=ja&id=sf.mfs_appointment_assistant_parent.htm)と[「Field Service の権限の割り当て」](https://help.salesforce.com/articleView?id=pfs_set_profiles_perms.htm&language=ja)を参照してください。



## FieldServiceDispatcherUser:<value>

Field Service Dispatcher 権限セットライセンスを追加します。1 ～ 25 の値を指定します。

### サポートされる数量

1 ～ 25、乗数: 1

### 詳細情報

詳細は、Salesforce ヘルプの[「Field Service の権限の割り当て」](https://help.salesforce.com/articleView?id=pfs_set_profiles_perms.htm&language=ja)を参照してください。



## FieldServiceLastMileUser:<value>

Field Service Last Mile 権限セットライセンスを追加します。1 ～ 25 の値を指定します。

### サポートされる数量

1 ～ 25、乗数: 1



## FieldServiceMobileExtension

Field Service Mobile Extension 権限セットライセンスを追加します。



## FieldServiceMobileUser:<value>

Field Service Mobile 権限セットライセンスを追加します。1 ～ 25 の値を指定します。

### サポートされる数量

1 ～ 25、乗数: 1

### 詳細情報

詳細は、Salesforce ヘルプの[「Field Service の権限の割り当て」](https://help.salesforce.com/articleView?id=pfs_set_profiles_perms.htm&language=ja)を参照してください。



## FieldServiceSchedulingUser:<value>

Field Service Scheduling 権限セットライセンスを追加します。1 ～ 25 の値を指定します。

### サポートされる数量

1 ～ 25、乗数: 1

### 詳細情報

詳細は、Salesforce ヘルプの[「Field Service の権限の割り当て」](https://help.salesforce.com/articleView?id=pfs_set_profiles_perms.htm&language=ja)を参照してください。



## FinanceLogging

ファイナンスログオブジェクトをスクラッチ組織に追加します。この機能は、ファイナンスログのために必要です。



## FinancialServicesCommunityUser:<値>

「Financial Services 保険コミュニティ」権限セットライセンスを追加し、Financial Services 保険コミュニティのコンポーネントとオブジェクトにアクセスできるようにします。1 ～ 10 の値を指定します。

### サポートされる数量

1 ～ 10、乗数: 1



## FinancialServicesInsuranceUser:<値>

「Financial Services 保険」権限セットライセンスを追加し、Financial Services 保険のコンポーネントとオブジェクトにアクセスできるようにします。1 ～ 10 の値を指定します。

### サポートされる数量

1 ～ 10、乗数: 1



## FinancialServicesUser:<値>

Financial Services Cloud の標準権限セットライセンスを追加します。この権限セットは、Lightning コンポーネントおよび Financial Services Cloud の標準バージョンにアクセスできるようにします。また、Salesforce の標準オブジェクトおよびカスタム Financial Services Cloud オブジェクトにもアクセスできるようにします。1 ～ 10 の値を指定します。

### サポートされる数量

1 ～ 10、乗数: 1



## FlowSites

Salesforce サイトとカスタマーポータルでフローを使用できるようにします。



## ForceComPlatform

1 件の Salesforce Platform ユーザーライセンスを追加します。



## ForecastEnableCustomField

商談に基づいた予測でカスタム通貨と顧客番号の項目を総計値として使用できるようにします。

### 詳細情報

Enterprise Edition と Unlimited Edition のスクラッチ組織で使用可能です。[設定] で [コラボレーション売上予測] を有効にする必要があります。詳細は Salesforce ヘルプの[「コラボレーション売上予測」を](https://help.salesforce.com/s/articleView?id=sf.forecasts3_intro.htm&language=ja)参照してください。



## FSCAlertFramework

スクラッチ組織で、Financial Services Cloud レコードアラートエンティティにアクセスできるようにします。

### 詳細情報

FSCComprehensivePsl ユーザーライセンスを 11 シートと、FSCComprehensiveAddOn アドオンライセンスを 11 シート提供します。

Financial Services Cloud と OmniStudio をインストールする必要があります。『Financial Services Cloud システム管理者ガイド』の[「レコードアラート」](https://developer.salesforce.com/docs/atlas.en-us.financial_services_cloud_admin_guide.meta/financial_services_cloud_admin_guide/fsc_admin_record_alerts.htm)を参照してください。



## FSCServiceProcess

Financial Services Cloud のサービスプロセススタジオ機能を有効化します。IndustriesServiceExcellenceAddOn ライセンスと FinancialServicesCloudStardardAddOn ライセンスのシートをそれぞれ 10 個提供します。この機能を有効にするには、[設定] で StandardServiceProcess 設定をオンにし、ユーザーに AccessToServiceProcess 権限を付与する必要もあります。



## 資金調達

Nonprofit Cloud for Fundraising 機能とオブジェクトへのアクセス権をユーザーに付与します。

### スクラッチ組織定義ファイル

資金調達を有効にするには、次の設定をスクラッチ組織定義ファイルに追加します。

```
{
    "orgName": "My Company",
    "edition": "Developer",
    "features": [
        "AccountingSubledgerGrowthEdition",
        "IndustriesActionPlan",
        "AnalyticsQueryService",
        "PublicSectorAccess",
        "Fundraising",
        "IndustriesSalesExcellenceAddOn",
        "IndustriesServiceExcellenceAddOn",
        "MarketingUser",
        "ProgramManagement",
        "OmniStudioDesigner",
        "OmniStudioRuntime",
        "EnableSetPasswordInApi",
        "PersonAccounts"
    ],
    "settings": {
        "lightningExperienceSettings": {
            "enableS1DesktopEnabled": true
        },
        "mobileSettings": {
            "enableS1EncryptedStoragePref2": false
        },
        "chatterSettings": {
            "enableChatter": true
        },
        "apexSettings": {
            "enableDisableParallelApexTesting": true
        },
        "enhancedNotesSettings": {
            "enableEnhancedNotes": true
        }
    }
}
```

### 詳細情報

詳細は、Salesforce ヘルプの [Nonprofit Cloud for Fundraising についての説明](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Nonprofit_Cloud_Fundraising.htm&language=ja)を参照してください。



## GenericStreaming

API バージョン 36.0 以前の汎用ストリーミング API を有効にします。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。



## GenStreamingEventsPerDay:<値>

API バージョン 36.0 以前の汎用ストリーミングを使用した場合の、24 時間以内に配信され、すべての CometD クライアントで共有されるイベント通知の最大数を増やします。10,000 ～ 50,000 の値を指定します。

### サポートされる数量

10,000 ～ 50,000、乗数: 1



## 助成金提供

Salesforce および Experience Cloud で助成金提供機能およびオブジェクトへのアクセス権をユーザーに付与します。

### 詳細情報

詳細は Salesforce ヘルプの[「Grantmaking (助成金提供)」](https://help.salesforce.com/s/articleView?id=sf.grmk_grantmaking.htm&language=ja)を参照してください。助成金提供機能を有効にするには、次の設定をスクラッチ組織定義ファイルに追加します。

```
{
  "features": ["Grantmaking"],
  "settings": {
    "IndustriesSettings": {
      "enableGrantmaking": true
    }
  }
}
```



## HealthCloudAddOn

Health Cloud を使用できるようにします。

### 詳細情報

詳細は、Salesforce ヘルプの[「Health Cloud の管理」](https://help.salesforce.com/apex/HTViewHelpDoc?id=healthcare_admin.htm&language=ja)を参照してください。



## HealthCloudEOLOverride

Salesforce は Spring ‘22 でより堅牢なリードオブジェクトに集中するため、Health Cloud CandidatePatient オブジェクトを廃止しました。このスクラッチ組織の機能では、その廃止を上書きしてこのオブジェクトにアクセスできます。

### 詳細情報

このスクラッチ組織機能を使用するには、Dev Hub 組織に HealthCloudEOLOverride 権限が必要です。詳細は、Salesforce ヘルプの[「患者候補データエンティティの廃止」](https://help.salesforce.com/s/articleView?id=000391944&type=1&language=ja)を参照してください。



## HealthCloudForCmty

Experience Cloud サイトでの Health Cloud の使用を有効にします。

### 詳細情報

詳細は、Salesforce ヘルプの[「Experience Cloud サイト」](https://help.salesforce.com/apex/HTViewHelpDoc?id=admin_communities.htm&language=ja)を参照してください。



## HealthCloudMedicationReconciliation

薬剤管理で薬剤確認をサポートできるようにします。

### 詳細情報

詳細は、Salesforce ヘルプの[「薬剤管理を有効化して薬剤確認を実行」](https://help.salesforce.com/s/articleView?id=sf.admin_medication_management_enable.htm&language=ja)を参照してください。



## HealthCloudPNMAddOn

プロバイダーネットワーク管理の使用を有効にします。

### 詳細情報

詳細は、Salesforce ヘルプの[「プロバイダーネットワーク管理」](https://help.salesforce.com/s/articleView?id=sf.admin_provider_network_management.htm&language=ja)を参照してください。



## HealthCloudUser

これによりスクラッチ組織は、1 人のユーザーの Health Cloud 権限セットライセンスと同等の Health Cloud オブジェクトおよび機能を使用できます。

### 詳細情報

詳細は、Salesforce ヘルプの[「Health Cloud 権限セットと権限セットライセンスの割り当て」](https://help.salesforce.com/s/articleView?id=sf.admin_permissionset_licenses_assign.htm&type=5&language=ja)を参照してください。



## HighVelocitySales

Sales Engagement ライセンスを提供し、Salesforce Inbox を有効にします。Sales Engagement は、生産性の高いワークスペースを使用して、インサイドセールスプロセスを最適化します。営業マネージャーは、さまざまな種別の見込み客を処理する方法を営業担当に示す、カスタムセールスプロセスを作成できます。営業担当は、優先リストや他の生産性向上機能によって見込み客をすばやく処理できます。Sales Engagement 機能はスクラッチ組織にリリースできますが、機能の設定はスクラッチ組織定義ファイルを介して更新できません。代わりに、Sales Engagement アプリケーションで設定を直接定義します。



## HoursBetweenCoverageJob:<値>

オブジェクトに対して共有継承の対象範囲レポートを実行する頻度 (時単位)。1 ～ 24 の値を指定します。

### サポートされる数量

1 ～ 24、乗数: 1



## IdentityProvisioningFeatures

Salesforce Identity のユーザープロビジョニングを使用できるようにします。



## IgnoreQueryParamWhitelist

クエリパラメーターの絞り込みルールで許可リストルールを無視します。有効である場合は、URL に任意のクエリパラメーターを追加できます。



メモ

可能な場合は、Equality の会社の値に一致するように、含めない用語を変更しました。顧客の実装に対する影響を回避するために、一部の用語は変更されていません。 



## IndustriesActionPlan

アクションプランのライセンスを提供します。アクションプランにより、ビジネスプロセスを完了するための ToDo やドキュメントチェックリスト項目を定義できます。

### 詳細情報

以前の名前: ActionPlan。

詳細と設定手順については、Salesforce ヘルプの[「アクションプランの有効化」](https://help.salesforce.com/articleView?id=fsc_action_plans.htm&language=ja)を参照してください。



## IndustriesBranchManagement

支店管理を使用することで、支店のマネージャーと管理者は Financial Services Cloud で支店、従業員、および顧客セグメントの仕事の成果を追跡できます。

### 詳細情報

支店管理アドオンライセンスとユーザー権限、および FSCComprehensivePsl ユーザーライセンスを 11 シート、FSCComprehensiveAddOn アドオンライセンスを 11 シート提供します。

Financial Services Cloud をインストールする必要があります。『Financial Services Cloud システム管理者ガイド』の[「Branch Management (支店管理)」](https://developer.salesforce.com/docs/atlas.en-us.financial_services_cloud_admin_guide.meta/financial_services_cloud_admin_guide/fsc_admin_branch.htm)を参照してください。



## IndustriesCompliantDataSharing

参加者管理や、データ共有の高度な設定へのアクセス権をユーザーに付与することで、規制や会社のポリシーへの準拠を強化します。

### 詳細情報

FinancialServicesCloudStandardAddOn アドオンライセンスのシートを 1 つ提供します。

Financial Services Cloud をインストールする必要があります。『Financial Services Cloud システム管理者ガイド』の[「準拠データ共有」](https://developer.salesforce.com/docs/atlas.en-us.financial_services_cloud_admin_guide.meta/financial_services_cloud_admin_guide/fsc_admin_cds.htm)を参照してください。



## IndustriesMfgTargets

販売計画を有効にします。販売計画を使用すると、継続的な期間にわたって商品の購入および販売に関する交渉を行うことができます。また、商品、価格、割引、数量に関するインサイトを得ることができます。さらに、注文と契約からのリアルタイム更新を使用して計画数、実績数、および収益を追跡することもできます。

### 詳細情報

詳細は Salesforce ヘルプの[「販売計画への営業の準拠の追跡」](https://help.salesforce.com/articleView?id=sa_admin_parent_concept.htm&type=5&language=ja)を参照してください。



## IndustriesManufacturingCmty

パートナーコミュニティユーザーによる使用を目的とした「コミュニティの製造販売計画」権限セットライセンスを提供します。また、システム管理者がコミュニティを作成するための製造業コミュニティテンプレートにもアクセスできるようにします。

### 詳細情報

詳細は Salesforce ヘルプの[「コミュニティを使用したパートナーコラボレーションの改善」](https://help.salesforce.com/articleView?id=sa_admin_communityoverview_concept.htm&type=5&language=ja)を参照してください。



## IndustriesMfgAccountForecast

取引先販売予測を有効にします。取引先販売予測により、注文、商談、販売計画に基づいて、取引先の販売予測を生成できます。また、取引先販売予測を使用することで、会社の要件に従って、販売予測を計算する数式を作成できます。

### 詳細情報

詳細は Salesforce ヘルプの[「計画を強化するための取引先販売予測の作成」](https://help.salesforce.com/articleView?id=af_admin_parent_concept.htm&type=5&language=ja)を参照してください。



## InsightsPlatform

CRM Analytics 用の CRM Analytics Plus ライセンスを有効にします。



## InsuranceCalculationUser

保険の計算機能を有効にします。BRERuntimeAddOn ライセンスと OmniStudioRuntime ライセンスのシートをそれぞれ 10 個提供します。また、OmniStudio ライセンスと BREPlatformAccess ライセンスのシートをそれぞれ 1 個提供します。



## InsuranceClaimMgmt

請求管理機能を有効にします。InsuranceClaimMgmtAddOn ライセンスのシートを 1 個提供します。

### 詳細情報

詳細は、Salesforce ヘルプの[「請求管理」](https://help.salesforce.com/s/articleView?id=ind.insurance_claims_617267.htm&type=5&language=ja)を参照してください。



## InsurancePolicyAdmin

保険契約管理機能を有効にします。InsurancePolicyAdministrationAddOn ライセンスのシートを 1 個提供します。

### 詳細情報

詳細は、Salesforce ヘルプの[「保険契約管理」](https://help.salesforce.com/s/articleView?id=ind.insurance_policy_administration_621128.htm&type=5&language=ja)を参照してください。



## IntelligentDocumentReader

インテリジェントドキュメントリーダーをスクラッチ組織で有効化および使用するために必要なライセンスを提供します。インテリジェントドキュメントリーダーは、AWS アカウントを使用して Amazon Textract で光学式文字認識を使ってデータを自動抽出します。

### 詳細情報

このスクラッチ組織機能を使用するには、Dev Hub 組織に EinsteinDocReader および BYOAForIFR 権限が必要です。インテリジェントドキュメントリーダーについては、Salesforce ヘルプの[「インテリジェントドキュメントリーダー」](https://help.salesforce.com/s/articleView?id=sf.intelligent_document_reader.htm&language=ja)を参照してください。



## Interaction

フローを有効にします。フローは、Salesforce 組織または外部システム内でデータを収集し、アクションを実行する Salesforce フローの一部です。Salesforce フローでは、画面フローと自動起動フローの 2 種類のフローが提供されます。

### 詳細情報

スクラッチ組織の [設定] メニューを使用した追加設定が必要です。



## IoT

IoT を有効にして、スクラッチ組織がプラットフォームイベントを消費してオーケストレーションとコンテキストを使用したビジネスワークフローとサービスワークフローを実行できるようにします。

### 詳細情報

スクラッチ組織定義ファイルにはメタデータ API 設定も指定する必要があります。



## JigsawUser

Jigsaw 機能のライセンスを 1 件提供します。



## ナレッジ

Salesforce ナレッジを有効にして、Web サイト訪問者、クライアント、パートナー、およびサービスエージェントに最上級のサポートを提供できるようにします。自社の情報を使用した知識ベースを作成して管理し、必要な時に必要な場所で安全に共有します。製品をデフォルトに戻す方法などのプロセスに関連した情報やよくある質問などを掲載した記事の知識ベースを構築してください。

### 詳細情報

詳細は Salesforce ヘルプの[「Salesforce ナレッジ」](https://help.salesforce.com/articleView?id=knowledge_whatis.htm&type=5&language=ja)を参照してください。



## LegacyLiveAgentRouting

チャットで従来の Live Agent ルーティングを有効にします。Salesforce Classic で Live Agent ルーティングを使用してチャットを行います。Lightning Experience のチャットでは、オムニチャネルを使用したルーティングが必要です。



## LightningSalesConsole

Lighting Sales Console ユーザーライセンスを 1 件追加します。



## LightningScheduler

Lightning Scheduler を有効にします。Lightning Scheduler は、Salesforce での予定のスケジュールを簡略化するためのツールを提供します。適切な担当者が割り当てられた顧客の予定 (対面、電話、またはビデオチャット) を適切な場所と時間にスケジュールすることで、パーソナライズした環境を作成します。

### 詳細情報

詳細は Salesforce ヘルプの[「Lightning Scheduler での予定の管理」](https://help.salesforce.com/articleView?id=ls_overview.htm&type=5&language=ja)を参照してください。



## LightningServiceConsole

Lightning サービスコンソールのライセンスをスクラッチ組織に割り当てて、ケースの管理をスピードアップするための Lightning サービスコンソール機能にアクセスできるようにします。

### 詳細情報

詳細は、Salesforce ヘルプの[「Lightning サービスコンソール」](https://help.salesforce.com/articleView?id=console_lex_service_intro.htm&language=ja)を参照してください。



## LiveAgent

Service Cloud でチャットを有効にします。Web ベースチャットを使用して、顧客をエージェントにすばやく接続することでリアルタイムサポートを実現します。



## LiveMessage

Service Cloud でメッセージングを有効にします。メッセージングでは、SMS テキストメッセージや Facebook Messenger などのアプリケーションを使用して、顧客をすばやくサポートします。



## LongLayoutSectionTitles

ページレイアウトセクションのタイトルに使用できる文字数を最大 80 文字にします。

### 詳細情報

この機能を有効にするには、Salesforce カスタマーサポートにご連絡ください。



## LoyaltyAnalytics

Analytics for Loyalty ライセンスを有効にします。Analytics for Loyalty アプリケーションには、ロイヤルティプログラムについてのアクション可能なインサイトが表示されます。

### 詳細情報

詳細は、Salesforce ヘルプの[「Analytics for Loyalty のリリースと使用」](https://help.salesforce.com/s/articleView?id=sf.analytics_loyalty_deploy_and_use.htm&language=ja)を参照してください。



## LoyaltyEngine

Loyalty Management Promotion Setup ライセンスを有効にします。プロモーション設定により、ロイヤルティプログラムマネージャーはロイヤルティプログラムプロセスを作成できます。ロイヤルティプログラムプロセスは、獲得種別と償還種別の受信および新規取引の処理方法を決定するのに役立ちます。

### 詳細情報

詳細は、Salesforce ヘルプの[「プロモーション設定を使用したプロセスの作成」](https://help.salesforce.com/s/articleView?id=sf.promotion_setup.htm&language=ja)を参照してください。



## LoyaltyManagementStarter

Loyalty Management - Starter ライセンスを有効にします。ロイヤルティプログラムを作成し、顧客の評価、報奨提供、維持を可能にするロイヤルティプログラム固有のプロセスを設定します。

### 詳細情報

詳細は、Salesforce ヘルプの[「ロイヤルティ管理」](https://help.salesforce.com/s/articleView?id=sf.loyaltyoverview.htm&language=ja)を参照してください。



## LoyaltyMaximumPartners:<value>

Loyalty Management - Starter ライセンスが有効な組織で、ロイヤルティプログラムに関連付けることができるロイヤルティプログラムパートナーの数を増やします。デフォルトおよび最大値は、1 です。

### サポートされる数量

0 ～ 1、乗数: 1



## LoyaltyMaximumPrograms:<value>

Loyalty Management - Starter ライセンスが有効な組織で作成できるロイヤルティプログラムの数を増やします。デフォルトおよび最大値は、1 です。

### サポートされる数量

0 ～ 1、乗数: 1



## LoyaltyMaxOrderLinePerHour:<value>

ロイヤルティプログラムプロセスで 1 時間あたりに累積的に処理できる注文品目の数を増やします。1 ～ 3,500,000 の値を指定します。

### サポートされる数量

1 ～ 3,500,000、乗数: 1



## LoyaltyMaxProcExecPerHour:<value>

ロイヤルティプログラムプロセスで 1 時間あたりに処理できる取引記録の数を増やします。1 ～ 500,000 の値を指定します。

### サポートされる数量

1 ～ 500,000、乗数: 1



## LoyaltyMaxTransactions:<value>

処理できる取引記録レコードの数を増やします。1 ～ 50,000,000 の値を指定します。

### サポートされる数量

1 ～ 50,000,000、乗数: 1



## LoyaltyMaxTrxnJournals:<value>

Loyalty Management - Start ライセンスが有効な組織に保存できる取引記録レコードの数を増やします。

### サポートされる数量

1 ～ 25,000,000、乗数: 1

### 詳細情報

詳細は、Salesforce ヘルプの[「取引記録の制限」](https://help.salesforce.com/s/articleView?id=sf.transaction_journal_limit_starter.htm&language=ja)を参照してください。



## マクロ

スクラッチ組織でマクロを有効にします。マクロを有効にしたら、Lightning コンソールにマクロブラウザーを追加し、よく使用するアクションを実行するための定義済み命令を設定して、複数の投稿に同時に適用できます。

### 詳細情報

詳細は Salesforce ヘルプの[「マクロの設定および使用」](https://help.salesforce.com/articleView?id=macros_def.htm&language=ja)を参照してください。



## MarketingUser

キャンペーンオブジェクトへのアクセス権を提供します。この設定を行わないと、キャンペーンは参照のみになります。



## MaxActiveDPEDefs:<value>

組織で有効化できるデータ処理エンジン定義の数を増やします。1 ～ 50 の値を指定します。

### サポートされる数量

1 ～ 50、乗数: 1



## MaxApexCodeSize:<値>

テスト以外の未管理 Apex コードのサイズ (MB) を制限します。デフォルト値の 10 よりも大きい値を使用するには、Salesforce カスタマーサポートにお問い合わせください。



## MaxAudTypeCriterionPerAud

利用者あたりの利用種別条件の使用可能数を制限します。デフォルト値は、10 です。



## MaxCustomLabels:<値>

カスタム表示ラベルの数 (1,000 単位) を制限します。この制限を 10 に設定すると、スクラッチ組織は 10,000 個のカスタム表示ラベルを持つことができます。1 ～ 15 の値を指定します。

### サポートされる数量

1 ～ 15、乗数: 1,000



## MaxDatasetLinksPerDT:<value>

決定表に関連付けることができるデータセットリンクの数を増やします。1 ～ 3 の値を指定します。

### サポートされる数量

1 ～ 3、乗数: 1



## MaxDataSourcesPerDPE:<value>

データ処理エンジン定義に含めることができるソースオブジェクトノードの数を増やします。1 ～ 50 の値を指定します。

### サポートされる数量

1 ～ 50、乗数: 1



## MaxDecisionTableAllowed:<value>

組織で作成できる決定表のルールの数を増やします。1 ～ 30 の値を指定します。

### サポートされる数量

1 ～ 30、乗数: 1



## MaxFavoritesAllowed:<値>

登録できるお気に入りの数を増やします。お気に入りは、ユーザーが登録する Salesforce ページへのショートカットです。ユーザーは、ヘッダーにある [お気に入り] リストドロップダウンをクリックすることで、自分のお気に入りを表示できます。0 ～ 200 の値を指定します。

### サポートされる数量

0 ～ 200、乗数: 1



## MaxFieldsPerNode:<value>

データ処理エンジン定義のノードに含めることができる項目の数を増やします。1 ～ 500 の値を指定します。

### サポートされる数量

1 ～ 500、乗数: 1



## MaxInputColumnsPerDT:<value>

決定表に含めることができる入力項目の数を増やします。1 ～ 10 の値を指定します。

### サポートされる数量

1 ～ 10、乗数: 1



## MaxLoyaltyProcessRules:<value>

組織で作成できるロイヤルティプログラムプロセスルールの数を増やします。1 ～ 20 の値を指定します。

### サポートされる数量

1 ～ 20、乗数: 1



## MaxNodesPerDPE:<value>

データ処理エンジン定義に含めることができるノードの数を増やします。1 ～ 500 の値を指定します。

### サポートされる数量

1 ～ 500、乗数: 1



## MaxNoOfLexThemesAllowed:<値>

使用できるテーマの数を増やします。テーマを使用することで、色、フォント、画像、サイズなどを設定できます。テーマのリストは、[設定] の [テーマとブランド設定] にあります。0 ～ 300 の値を指定します。

### サポートされる数量

0 ～ 300、乗数: 1



## MaxOutputColumnsPerDT:<value>

決定表に含めることができる出力項目の数を増やします。1 ～ 5 の値を指定します。

### サポートされる数量

1 ～ 5、乗数: 1



## MaxSourceObjectPerDSL:<value>

決定表のデータセットリンクで選択できるソースオブジェクトの数を増やします。1 ～ 5 の値を指定します。

### サポートされる数量

1 ～ 5、乗数: 1



## MaxStreamingTopics:<値>

24 時間以内に配信され、すべての CometD クライアントで共有される PushTopic イベント通知の最大数を増やします。40 ～ 100 の値を指定します。

### サポートされる数量

40 ～ 100、乗数: 1



## MaxUserNavItemsAllowed:<値>

ユーザーがナビゲーションバーに追加できるナビゲーション項目の数を増やします。0 ～ 500 の値を指定します。

### サポートされる数量

0 ～ 500、乗数: 1



## MaxUserStreamingChannels:<値>

ユーザー定義の汎用ストリーミングチャネルの最大数を増やします。20 ～ 1,000 の値を指定します。

### サポートされる数量

20 ～ 1,000、乗数: 1



## MaxWritebacksPerDPE:<value>

データ処理エンジン定義に含めることができる書き戻しオブジェクトノードの数を増やします。1 ～ 50 の値を指定します。

### サポートされる数量

1 ～ 10、乗数: 1



## MedVisDescriptorLimit:<値>

オブジェクトに適用される共有継承のレコードあたりの共有定義の数を増やします。150 ～ 1,600 の値を指定します。

### サポートされる数量

150 ～ 1,600、乗数: 1



## MinKeyRotationInterval

暗号化鍵素材の循環間隔を 60 秒に 1 回設定します。この機能を指定しない場合、循環間隔は、検索インデックスの鍵素材では 604,800 秒 (7 日) に 1 回、他のすべての鍵素材では 86,400 秒 (24 時間) に 1 回にデフォルト設定されます。

### 詳細情報

スクラッチ組織で [設定] メニューを使用して、[PlatformEncryption](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_def_file_config_values.htm#so_platformencryption) およびいくつかの設定を有効にする必要があります。Salesforce ヘルプの[「Shield Platform Encryption に必要なユーザー権限」](https://help.salesforce.com/articleView?id=security_pe_permissions.htm&language=ja)と[「Salesforce を使用したテナントの秘密の生成」](https://help.salesforce.com/articleView?id=security_pe_ui_setup.htm&language=ja)を参照してください。



## MobileExtMaxFileSizeMB:<値>

Field Service Mobile 拡張機能のファイルサイズ (MB) を増やします。1 ～ 2,000 の値を指定します。

### サポートされる数量

1 ～ 2,000、乗数: 1



## MobileSecurity

拡張モバイルセキュリティを有効にします。拡張モバイルセキュリティでは、ポリシーの範囲を制御して、組織のニーズに合わせて調整されたセキュリティソリューションを作成できます。オペレーティングシステムのバージョン、アプリケーションのバージョン、デバイスおよびネットワークのセキュリティに基づいてユーザーアクセスを制限できます。違反の重要度を指定することもできます。



## MultiLevelMasterDetail

1 つのオブジェクト (子、または「従」) と別のオブジェクト (親、または「主」) の間に特殊な親子リレーションを作成できるようにします。



## MutualAuthentication

相互認証の受信要求の検証でクライアント証明書を要求します。



## MyTrailhead

スクラッチ組織で myTrailhead イネーブルメントサイトにアクセスできるようにします。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
{
    "orgName": "Acme",
    "edition": "Enterprise",
    "features": ["MyTrailhead"],
    "settings": {
        "trailheadSettings": {
            "enableMyTrailheadPref": true
            }  
        }  
    }
```

### 詳細情報

Salesforce ヘルプ: [イネーブルメントサイト (myTrailhead)](https://help.salesforce.com/s/articleView?id=sf.mth_intro.htm&language=ja)



## NonprofitCloudCaseManagementUser

Salesforce.org の Nonprofit Cloud Case Management 管理パッケージを使用および設定するために必要な権限セットライセンスを提供します。これにより、パッケージをスクラッチ組織にインストールできます。

### 詳細情報

インストールと設定の手順については、[「Salesforce.org Nonprofit Cloud Case Management (Salesforce.org の Nonprofit Cloud Case Management)」](https://powerofus.force.com/s/article/CM-Documentation)を参照してください。



## NumPlatformEvents:<値>

1 つの組織で作成できるプラットフォームイベント定義の最大数を増やします。5 ～ 20 の値を指定します。

### サポートされる数量

5 ～ 20、乗数: 1



## ObjectLinking

ルールを作成して、チャネルインタラクションを、顧客の取引先責任者、リード、個人取引先などのオブジェクトにすばやくリンクします (ベータ)。



## OrderManagement

Salesforce Order Management ライセンスを提供します。Order Management (注文管理) は、注文捕捉、履行、納入、支払処理、サービスなど、注文ライフサイクルのすべての側面を処理するための中央ハブです。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。

注文管理を設定して次の機能を使用する場合は、該当する機能をスクラッチ組織で有効にします。

- MultiCurrency
- PersonAccounts
- ProcessBuilder
- StateAndCountryPicklist

スクラッチ組織で [設定] メニューを使用した設定が必要です。インストールと設定の手順については、Salesforce ヘルプの[「Salesforce Order Management」](https://help.salesforce.com/s/articleView?id=sf.om_order_management.htm&type=5&language=ja)を参照してください。



メモ

実装プロセスでは、[設定] で注文および注文管理機能の複数のトグルをオンにする必要があります。スクラッチ組織でトグルをオンにするには、スクラッチ組織の定義ファイルにメタデータ設定を含める必要があります。これらの設定についての詳細は、『メタデータ API 開発者ガイド』の[「OrderSettings」](https://developer.salesforce.com/docs/atlas.ja-jp.api_meta.meta/api_meta/meta_ordersettings.htm)および[「OrderManagementSettings」](https://developer.salesforce.com/docs/atlas.ja-jp.api_meta.meta/api_meta/meta_ordermanagementsettings.htm)を参照してください。



## OrderSaveLogicEnabled

注文の新規保存方式のスクラッチ組織サポートを有効にします。OrderSaveLogicEnabled では、注文の新規保存方式のみがサポートされます。スクラッチ組織で注文の旧保存方式と新規保存方式の両方が必要な場合は、OrderSaveBehaviorBoth を使用します。

### スクラッチ組織定義ファイル

OrderSaveLogicEnabled を有効にするには、スクラッチ組織の定義ファイルを更新します。

```
{
  "features": ["OrderSaveLogicEnabled"],
  "settings": {
    "orderSettings": {
      "enableOrders": true
    }
  }
}
```



## OrderSaveBehaviorBoth

注文の新規保存方式と旧保存方式の両方のスクラッチ組織サポートを有効にします。

### スクラッチ組織定義ファイル

OrderSaveLogicEnabled を有効にするには、スクラッチ組織の定義ファイルを更新します。

```
{
   "features": ["OrderSaveBehaviorBoth"],
  "settings": {
    "orderSettings": {
      "enableOrders": true
    }
  }
}
```



## OutboundMessageHTTPSession

[送信セッション ID] オプションが選択されている送信メッセージ定義で HTTP エンドポイント URL を使用できるようにします。



## OutcomeManagement

Salesforce の結果管理機能とオブジェクトへのアクセス権をユーザーに付与します。

### 詳細情報

詳細は、Salesforce ヘルプの[「結果管理」](https://help.salesforce.com/s/articleView?id=sf.outcome_management.htm&language=ja)を参照してください。結果管理を有効にするには、次の設定をスクラッチ組織定義ファイルに追加します。

```
{
  "features": ["OutcomeManagement"],
  "settings": {
    "IndustriesSettings": {
      "enableOutcomes": true
    }
  }
}
```



## PardotScFeaturesCampaignInfluence

Pardot ユーザーに対して追加のキャンペーンインフルエンスモデル、つまり初回接触、最終回接触、均等分布を有効にします。



## PersonAccounts

スクラッチ組織で個人取引先を有効にします。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。



## PipelineInspection

パイプラインインスペクションを有効にします。パイプラインインスペクションは、総計値、商談、最近の変更のハイライトを示すパイプラインの統合ビューです。

### 詳細情報

Enterprise Edition スクラッチ組織で使用できます。



## PlatformCache

Enables プラットフォームキャッシュを有効にして、3 MB のキャッシュを割り当てます。Lightning プラットフォームキャッシュレイヤーを使用すると、Salesforce セッションおよび組織データをキャッシュするときのパフォーマンスと信頼性が向上します。

### 詳細情報

詳細は、『Apex コード開発者ガイド』の[「プラットフォームキャッシュ」](https://developer.salesforce.com/docs/atlas.ja-jp.apexcode.meta/apexcode/apex_cache_namespace_overview.htm)を参照してください。



## PlatformConnect:<値>

Salesforce Connect を有効にして、ユーザーが Salesforce 組織外に保存されているデータを表示、検索、変更できるようにします。1 ～ 5 の値を指定します。

### サポートされる数量

1 ～ 5、乗数: 1



## PlatformEncryption

Shield Platform Encryption は、保存されているデータを暗号化します。鍵素材を管理して、項目、ファイル、および他のデータを暗号化できます。



## PlatformEventsPerDay:<value>

24 時間以内に配信され、すべての CometD クライアントで共有される標準量のプラットフォームイベント通知の最大数を増やします。10,000 ～ 50,000 の値を指定します。

### サポートされる数量

10,000 ～ 50,000、乗数: 1



## ProcessBuilder

ビジネスプロセスを自動化できる Salesforce フローツールであるプロセスビルダーを有効にします。

### 詳細情報

スクラッチ組織の [設定] メニューを使用した追加設定が必要です。

詳細は、Salesforce ヘルプの[「プロセスビルダー」](https://help.salesforce.com/articleView?id=process_overview.htm&language=ja)を参照してください。



## ProductsAndSchedules

スクラッチ組織で商品スケジュールを有効にします。この機能を有効にすると、商品に対してデフォルトの商品スケジュールを作成できるようになります。ユーザーは、商談の個別商品のスケジュールも作成できます。



## ProductCatalogManagementAddOn

商品カタログ管理機能とオブジェクトへの参照・更新アクセス権を有効にします。

### 詳細情報

Developer Edition と Enterprise Edition のスクラッチ組で使用できます。商品カタログ管理のアドオンライセンスを 1 つ提供します。



## ProductCatalogManagementViewerAddOn

商品カタログ管理機能とオブジェクトへの参照アクセス権を有効にします。

### 詳細情報

Developer Edition と Enterprise Edition のスクラッチ組で使用できます。商品カタログ管理閲覧者のアドオンライセンスを 1 つ提供します。



## ProductCatalogManagementPCAddOn

スクラッチ組織の Partner Community ユーザーに対して、商品カタログ管理機能とオブジェクトへの参照アクセス権を有効にします。

### 詳細情報

- Developer Edition と Enterprise Edition のスクラッチ組で使用できます。
- 商品カタログ管理のアドオンライセンスを 1 つ提供します。
- Partner Community ユーザーを設定する必要があります。Partner Community ユーザーに、商品カタログ管理パートナーコミュニティのアドオンライセンスが付与されている必要があります。



## ProgramManagement

すべてのプログラム管理およびケース管理機能とオブジェクトへのアクセスを可能にします。

### 詳細情報

ProgramManagement を有効にするには、次の設定をスクラッチ組織定義ファイルに追加します。

```
{
  "orgName": "Sample Org" ,
  "edition": "Enterprise",
  "features": ["ProgramManagement"],
  "settings": {
    "IndustriesSettings": {
      "enableBenefitManagementPreference": true,
      "enableBenefitAndGoalSharingPref": true,
      "enableCarePlansPreference": true
    }
  }
}
```

または、組織の設定を手動で有効にします。Salesforce ヘルプの[「Enable Program Management (プログラム管理の有効化)」](https://help.salesforce.com/s/articleView?id=sfdo.PM_NP_Enable_Program_Management.htm&type=5&language=ja)を参照してください。



## ProviderFreePlatformCache

セキュリティレビューに合格した管理パッケージには、3 MB の無料のプラットフォームキャッシュ容量が提供されます。この機能は、プロバイダー無料容量という容量種別で使用でき、Developer Edition 組織で自動的に有効になります。プロバイダー無料容量をプラットフォームキャッシュ区分に割り当て、管理パッケージに追加します。

### 詳細情報

詳細は、Salesforce ヘルプの[「プロバイダー無料容量を使用したプラットフォームキャッシュ区分の設定」](https://help.salesforce.com/articleView?id=data_platform_cache_setup_provider_capacity.htm&type=5&language=ja)を参照してください。



## PublicSectorAccess

すべての公共セクターの機能とオブジェクトへのアクセスを有効にします。



## PublicSectorApplicationUsageCreditsAddOn

価格設定に基づいて、公共セクターアプリケーションの追加利用を有効にします。



## PublicSectorSiteTemplate

公共セクターユーザーに対して、利用可能なテンプレートから Experience Cloud サイトを構築するためのアクセスを許可します。



## RecordTypes

レコードタイプ機能を有効にします。レコードタイプを使用すると、さまざまなビジネスプロセス、選択リストの値、およびページレイアウトを、さまざまなユーザーに提供できます。



## RefreshOnInvalidSession

ユーザーセッションが無効な場合に Lightning ページの自動更新を有効にします。ただし、ページが新しいトークンを検出すると、そのトークンを設定して更新せずに続行を試みます。



## RevSubscriptionManagement

サブスクリプション管理を有効にします。サブスクリプション管理は、B2B サブスクリプションおよび 1 回限りの販売に対応した API ファーストの商品 -to- キャッシュソリューションです。

### 詳細情報

Enterprise および Developer スクラッチ組織で使用できます。スクラッチ組織でサブスクリプション管理を有効にするには、スクラッチ組織定義ファイルに次の設定を追加します。

```
"settings": {
    ...
    "subscriptionManagementSettings": {
      "enableSubscriptionManagement": true
    },
    ...
  }
```

サブスクリプション管理についての詳細は、https://developer.salesforce.com/docs/revenue/subscription-management/overview を参照してください。



## S1ClientComponentCacheSize

組織で Lightning コンポーネントを 5 ページまでキャッシュできるようにします。



## SalesCloudEinstein

Sales Cloud Einstein 機能と Salesforce Inbox を有効にします。Sales Cloud Einstein は、営業プロセスの各プロセスに AI を適用します。

### 詳細情報

Enterprise Edition スクラッチ組織で使用できます。

詳細は Salesforce ヘルプの[「Sales Cloud Einstein」](https://help.salesforce.com/articleView?id=einstein_sales.htm&type=5&language=ja)を参照してください。



## SalesforceContentUser

Salesforce コンテンツ機能へのアクセスを有効にします。



## SalesforceFeedbackManagementStarter

Salesforce Feedback Management - Starter 機能を使用するためのライセンスを提供します。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。Salesforce Feedback Management - Starter 機能を使用するには、アンケートを有効にし、Salesforce Advanced Features Starter ユーザー権限をスクラッチ組織ユーザーに割り当てます。アンケートと設定の手順を有効にする方法についての詳細は、Salesforce ヘルプの[「アンケートの有効化とアンケート設定の構成」](https://help.salesforce.com/s/articleView?id=sf.task_enable_surveys.htm&type=5&language=ja)および[「ユーザー権限の割り当て」](https://help.salesforce.com/s/articleView?id=sf.concept_setup_sfm_profiles.htm&type=5&language=ja)を参照してください。



## SalesforceIdentityForCommunities

ログインやセルフ登録などの Salesforce Identity コンポーネントをエクスペリエンスビルダーに追加します。この機能は、Aura コンポーネントでは必須です。



## SalesUser

Sales Cloud 機能のライセンスを提供します。



## SAML20SingleLogout

SAML 2.0 シングルログアウトを使用できるようにします。



## SCIMProtocol

SCIM プロトコルベース API のアクセスサポートを有効にします。



## SecurityEventEnabled

イベントモニタリングでセキュリティイベントへのアクセスを有効にします。



## SentimentInsightsFeature

センチメントインサイトをスクラッチ組織で有効化および使用するために必要なライセンスを提供します。センチメントインサイトを使用すると、顧客のセンチメントを分析して、アクション可能なインサイトを取得してセンチメントを改善できます。

### 詳細情報

このスクラッチ組織機能を使用するには、Dev Hub 組織に IESentimentAnalysis、AwsSentimentAnalysis、BYOAForSentiment、IESentimentAnalysisEnabled 権限が必要です。センチメントインサイトについては、Salesforce ヘルプの[「センチメントインサイト」](https://help.salesforce.com/s/articleView?id=sf.sentiment_insights.htm&language=ja)を参照してください。



## ServiceCatalog

従業員サービスカタログを有効にすると、従業員向けの製品とサービスのカタログを作成できます。また、それらの製品およびサービスの従業員の要求を承認済みの文書化された注文にすることもできます。

### 詳細情報

このスクラッチ組織機能を使用するには、Dev Hub 組織に ServiceCatalog 権限が必要です。詳細は、[「従業員サービスカタログの使用開始」](https://help.salesforce.com/s/articleView?id=sf.esc_get_started_with_employee_service_catalog.htm&language=ja)を参照してください。



## ServiceCloud

Service Cloud ライセンスをスクラッチ組織に割り当てて、メール、電話、ソーシャルメディア、オンラインコミュニティ、チャット、テキストなど、顧客からの連絡方法を選択できるようにします。



## ServiceCloudVoicePartnerTelephony

パートナーテレフォニーを使用する Service Cloud Voice のアドオンライセンスをスクラッチ組織に割り当てると、サポートされているテレフォニープロバイダーと統合する Service Cloud Voice コンタクトセンターを設定できます。1 ～ 50 の値を指定します。

### サポートされる数量

1 ～ 50、乗数: 1

### 詳細情報

設定手順については、Salesforce ヘルプの[「パートナーテレフォニーを使用する Service Cloud Voice」](https://help.salesforce.com/articleView?id=sf.voice_pt_setup.htm&language=ja)を参照してください。



## ServiceUser

Service Cloud User ライセンスを 1 件追加して、Service Cloud 機能にアクセスできるようにします。



## SessionIdInLogEnabled

Apex デバッグログを有効にして、セッション ID を含めます。無効である場合、デバッグログではセッション ID が「SESSION_ID_REMOVED」に置き換えられます。



## SFDOInsightsDataIntegrityUser

ライセンスを Salesforce.org の Insights Platform Data Integrity 管理パッケージに提供します。これにより、パッケージをスクラッチ組織にインストールできます。

### 詳細情報

インストールと設定の手順については、[「Salesforce.org Insights Platform Data Integrity (Salesforce.org の Insights Platform Data Integrity)」](https://powerofus.force.com/s/article/IP-Documentation)ヘルプを参照してください。



## SharedActivities

ユーザーが複数取引先責任者を ToDo と行動に関連付けられるようにします。

### 詳細情報

インストールと設定の手順についての詳細は、Salesforce ヘルプの[「Shared Activities の有効化に関する考慮事項」](https://help.salesforce.com/s/articleView?id=sf.activities_shared_considerations.htm&type=5&language=ja)を参照してください。



## サイト

Salesforce サイトを有効にして、Salesforce 組織と直接統合される公開 Web サイトとアプリケーションを作成できるようにします。ユーザーは、ユーザー名とパスワードを使用してログインする必要はありません。

### 詳細情報

スクラッチ組織ではサイトとコミュニティを作成できますが、www.example.com のようなカスタムドメインはサポートされません。



## SocialCustomerService

ソーシャルカスタマーサービスを有効にし、投稿のデフォルトを設定して、Starter Pack を有効にするか、または Social Studio アカウントにサインインします。



## StateAndCountryPicklist

州選択リストと国/テリトリー選択リストを有効にします。州選択リストや国/テリトリー選択リストを使用すると、都道府県、国、テリトリーのデータをテキスト項目に入力する代わりに、事前定義の標準化されたリストから選択できます。



## StreamingAPI

ストリーミング API を有効化します。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。



## StreamingEventsPerDay:<値>

24 時間以内に配信され、すべての CometD クライアントで共有される PushTopic イベント通知の最大数を増やします (API バージョン 36.0 以前)。10,000 ～ 50,000 の値を指定します。

### サポートされる数量

10,000 ～ 50,000、乗数: 1



## SubPerStreamingChannel:<値>

汎用ストリーミングチャネルでの同時クライアント (登録者) の最大数を増やします (API バージョン 36.0 以前)。20 ～ 4,000 の値を指定します。

### サポートされる数量

20 ～ 4,000、乗数: 1



## SubPerStreamingTopic:<value>

PushTopic ストリーミングチャネルでの同時クライアント (登録者) の最大数を増やします (API バージョン 36.0 以前)。20 ～ 4,000 の値を指定します。

### サポートされる数量

20 ～ 4,000、乗数: 1



## SurveyAdvancedFeatures

Salesforce Feedback Management - Growth ライセンスで使用できる機能のライセンスを有効にします。

### 詳細情報

Enterprise および Developer Edition のスクラッチ組織で使用できます。Salesforce Feedback Management - Growth 機能を使用するには、アンケートを有効にし、Salesforce Surveys Advanced Features ユーザー権限をスクラッチ組織ユーザーに割り当てます。アンケートと設定の手順を有効にする方法についての詳細は、Salesforce ヘルプの[「アンケートの有効化とアンケート設定の構成」](https://help.salesforce.com/s/articleView?id=sf.task_enable_surveys.htm&type=5&language=ja)および[「ユーザー権限の割り当て」](https://help.salesforce.com/s/articleView?id=sf.concept_setup_sfm_profiles.htm&type=5&language=ja)を参照してください。



## SustainabilityCloud

Sustainability Cloud をインストールして設定するために必要な権限セットライセンスと権限セットを提供します。CRM Analytics と CRM Analytics テンプレートを有効にする、または使用するには、DevelopmentWave スクラッチ組織の機能を含めます。

### 詳細情報

インストールと設定の手順については、Salesforce ヘルプの「Net Zero Cloud の設定および管理」ガイドの[「Sustainability Cloud の従来のドキュメント」](https://help.salesforce.com/apex/HTViewHelpDoc?id=sustainability_cloud_legacy_documentation.htm&language=ja)を参照してください。



## SustainabilityApp

Net Zero Cloud を設定するために必要な権限セットライセンスと権限セットを提供します。Tableau CRM と Tableau CRM テンプレートを有効にする、または使用するには、DevelopmentWave スクラッチ組織の機能を含めます。

### スクラッチ組織定義ファイル

スクラッチ組織定義ファイルに次のオプションを追加します。

```
{
  "orgName": "net zero scratch org",
  "edition": "Developer",
  "features": ["SustainabilityApp"],
  "settings": {
    "industriesSettings":{
      "enableSustainabilityCloud": true,
      "enableSCCarbonAccounting" : true
    }
  }
}
```

### 詳細情報

設定の手順については、Salesforce ヘルプの「Net Zero Cloud の設定および管理」ガイドの[「Net Zero Cloud の設定」](https://help.salesforce.com/s/articleView?id=netzero_admin.htm&language=ja)を参照してください。



## TCRMforSustainability

Tableau CRM を有効にして、Net Zero Analytics アプリケーションを管理するために必要なすべての権限を有効にします。ユーザーの Analytics アプリケーションを作成して共有すると、環境会計と財務会計を一致させることができます。

### 詳細情報

詳細は、Salesforce ヘルプの「Net Zero Cloud の設定および管理」ガイドの[「Net Zero Analytics のリリース」](https://help.salesforce.com/s/articleView?id=sf.netzero_admin_analytics_deploy.htm&language=ja)を参照してください。



## TimelineConditionsLimit

イベント種別あたりのタイムラインレコード表示条件の数を 3 に制限します。

### 詳細情報

詳細は、Salesforce ヘルプの[「拡張スケジュールによる総合的な患者ケアの提供」](https://help.salesforce.com/s/articleView?id=sf.hc_timeline.htm&language=ja)を参照してください。



## TimelineEventLimit

タイムラインに表示するイベント種別の数を 5 に制限します。

### 詳細情報

詳細は、Salesforce ヘルプの[「拡張スケジュールによる総合的な患者ケアの提供」](https://help.salesforce.com/s/articleView?id=sf.hc_timeline.htm&language=ja)を参照してください。



## TimelineRecordTypeLimit

イベント種別あたりの関連オブジェクトレコードタイプの数を 3 に制限します。

### 詳細情報

詳細は、Salesforce ヘルプの[「拡張スケジュールによる総合的な患者ケアの提供」](https://help.salesforce.com/s/articleView?id=sf.hc_timeline.htm&language=ja)を参照してください。



## TimeSheetTemplateSettings

タイムシートテンプレートにより、タイムシートを自動的に作成するように設定できます。たとえば、開始日と終了日を設定するテンプレートを作成できます。テンプレートをユーザープロファイルに割り当てることで、適切なユーザーに対してタイムシートが作成されます。

### 詳細情報

設定の手順については、Salesforce ヘルプの[「タイムシートテンプレートの作成」](https://help.salesforce.com/articleView?id=fs_create_timesheets.htm&type=5&language=ja)を参照してください。



## TransactionFinalizers

Apex Finalizer を実装して、キュー可能 Apex ジョブに関連付けます。

### 詳細情報



メモ

この機能は現在オープンパイロットであり、制限があります。

詳細は、『Apex コード開発者ガイド』の[「Transaction Finalizers (パイロット)」](https://developer.salesforce.com/docs/atlas.ja-jp.apexcode.meta/apexcode/apex_transaction_finalizers.htm)を参照してください。



## WaveMaxCurrency

CRM Analytics でサポートされる通貨の最大数を増やします。1 ～ 5 の値を指定します。



## WavePlatform

Wave プラットフォームライセンスを有効にします。



## Workflow

ワークフローを有効にして、標準的な内部の手続きやプロセスを自動化できるようにします。

### 詳細情報

スクラッチ組織の [設定] メニューを使用した追加設定が必要です。



## WorkflowFlowActionFeature

ワークフローアクションからフローを起動できるようにします。

### 詳細情報

この設定は、組織でフロートリガーワークフローアクションのパイロットプログラムを有効にした場合にのみサポートされます。パイロットを有効にした場合は、引き続きフロートリガーワークフローアクションを作成および編集できます。

パイロットを有効にしなかった場合は、代わりにスクラッチ組織機能のプロセスビルダーでフローアクションを使用してください。



## WorkplaceCommandCenterUser

Employee、Crisis、EmployeeCrisisAssessment などのオブジェクトへのアクセスを含め、Workplace Command Center の機能にアクセスできるようにします。

### 詳細情報

インストールと設定の手順についての詳細は、『Work.com の Workplace Command Center 開発者ガイド』の[「Work.com 開発組織の設定」](https://developer.salesforce.com/docs/atlas.ja-jp.workdotcom_dev_guide.meta/workdotcom_dev_guide/wdc_cc_setup_dev_org.htm)を参照してください。



## WorkThanksPref

Chatter で感謝機能を有効にします。