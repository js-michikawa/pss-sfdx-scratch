# Timeline 設定ガイド

## 概要

Salesforce Timeline は、関連オブジェクトのイベントを時系列で表示する機能です。PSS 環境では、市民とのやり取りやケースの履歴を可視化するために有効です。

## Timeline の有効化手順

### 1. Timeline Configuration を有効化

1. Setup を開く
2. Quick Find で「Timeline」を検索
3. **Timeline** を選択
4. **Timeline Configuration** を有効化
   - ⚠️ **注意**: 一度有効化すると無効化できません

### 2. Timeline の作成

1. **New Timeline** をクリック
2. 以下の情報を設定:
   - **Timeline Name**: わかりやすい名前 (例: "Case Timeline")
   - **API Name**: 自動生成または手動入力
   - **Base Object**: タイムラインの基準となるオブジェクト (例: Case)

### 3. グローバル設定

- **Show Age**: レコードの経過時間を表示する場合は有効化

### 4. イベント表示項目の設定

関連オブジェクトから表示する項目を選択:
- **Title Field**: イベントのタイトル (例: Subject)
- **Subtitle Field**: サブタイトル (例: Description)
- **Timestamp Field**: タイムスタンプ (例: Created Date) - インデックス化された項目を推奨
- **Summary Field**: 概要フィールド

### 5. 関連オブジェクトの追加

- 最大5つの関連オブジェクトを追加可能
- Base Object と直接のルックアップ関係が必要
- 各オブジェクトにつき最大3つのレコードタイプを選択可能

### 6. 表示フィールドの選択

Timeline に表示したいフィールドと関連リストを選択

### 7. Timeline の有効化

**Activate** をクリックして Timeline を有効化

### 8. Lightning ページへの追加

1. Lightning App Builder を開く
2. 対象のレコードページを編集
3. **Timeline** コンポーネントをページに追加
4. 作成した Timeline 設定を選択
5. ページを保存して有効化

## メタデータの取得

Timeline 設定は `TimelineObjectDefinition` メタデータとして保存されます。

### 取得コマンド

```bash
# Timeline メタデータを取得
sf project retrieve start --metadata TimelineObjectDefinition --wait 30
```

### メタデータの場所

```
force-app/main/default/timelineObjectDefinitions/
└── YourTimeline.timelineObjectDefinition-meta.xml
```

## Activity Timeline の設定

Activity Timeline は、タスク、イベント、通話記録、メールを時系列で表示します。

### 有効化手順

1. Setup > Quick Find で「Record Page Settings」を検索
2. **Default Activities View** を **Activity Timeline** に設定
3. 保存

## ベストプラクティス

### PSS 環境での推奨設定

1. **Case Timeline**
   - Base Object: Case
   - 関連オブジェクト: Email Message, Task, Event, Case Comment

2. **Account Timeline** (市民/組織)
   - Base Object: Account
   - 関連オブジェクト: Case, Opportunity, Task, Event

3. **Inspection Timeline** (検査)
   - Base Object: Inspection (カスタムオブジェクト)
   - 関連オブジェクト: Inspection Item, Task, Event

## トラブルシューティング

### Timeline が表示されない

- Lightning ページに Timeline コンポーネントが追加されているか確認
- Timeline が Activate されているか確認
- ユーザーに適切な権限があるか確認

### 関連オブジェクトが表示されない

- Base Object との直接のルックアップ関係があるか確認
- 関連オブジェクトのレコードタイプが選択されているか確認

## 参考リンク

- [Salesforce Help: Set Up Timeline](https://help.salesforce.com/s/articleView?id=sf.timeline_setup.htm)
- [TimelineObjectDefinition Metadata API](https://developer.salesforce.com/docs/atlas.en-us.api_meta.meta/api_meta/meta_timelineobjectdefinition.htm)
