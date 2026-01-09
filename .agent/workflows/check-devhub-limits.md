---
description: Dev Hub のスクラッチ組織作成制限を確認
---

# Dev Hub 制限確認ワークフロー

スクラッチ組織を作成する前に、Dev Hub の残り作成回数を確認します。

## コマンド

```bash
# Dev Hub の制限を確認
sf org list limits --target-org DevHub
```

## 確認する項目

### 重要な制限

1. **DailyScratchOrgs**
   - 1日あたりのスクラッチ組織作成数
   - デフォルト: 6個/日 (Developer Edition)
   - Enterprise Edition: 200個/日

2. **ActiveScratchOrgs**
   - 同時にアクティブにできるスクラッチ組織数
   - デフォルト: 3個 (Developer Edition)
   - Enterprise Edition: 40個

## 出力例

```
Name                          Max    Remaining
────────────────────────────  ─────  ─────────
DailyScratchOrgs              6      4
ActiveScratchOrgs             3      1
```

## 制限に達した場合の対処法

### DailyScratchOrgs の制限に達した場合

- 翌日まで待つ
- 既存のスクラッチ組織を削除しても、この制限は回復しない
- 制限は UTC 時間でリセットされる

### ActiveScratchOrgs の制限に達した場合

```bash
# 不要なスクラッチ組織を削除
sf org delete scratch --target-org <alias> --no-prompt

# または、全てのスクラッチ組織を確認して削除
sf org list --all
```

## ベストプラクティス

1. **作成前に必ず確認**: スクラッチ組織を作成する前に残数を確認する
2. **不要な組織は削除**: 使わなくなったスクラッチ組織は速やかに削除する
3. **期限を短く設定**: 必要最小限の期間 (7日など) で作成する
4. **計画的に作成**: 1日の作成回数を計画的に使用する

## ナレッジ

- スクラッチ組織の作成回数は **UTC 時間** でリセットされる
- 日本時間の午前9時 (JST) = UTC 0時
- Developer Edition の制限は厳しいため、慎重に使用する
- 検証が必要な場合は、既存のスクラッチ組織を削除してから新規作成する
