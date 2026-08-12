# Issueデータ仕様

## 原本の項目

| 項目 | 内容 | 例 |
|---|---|---|
| `id` | 教材内で一意のID | `SYN-ISSUE-001` |
| `title` | GitHub Issueのタイトル | `[SYNTH][LAB-TV-001] 起動後に映像が表示されない` |
| `state` | 公開後の状態 | `open` / `closed` |
| `labels` | 分類ラベル4個 | `kind:bug` など |
| `body` | Issue本文 | Markdown |

CSV/JSONスナップショットには、合成情報であることを機械的にも確認できるよう、`model`、`firmware`、`evidence_id`も記録します。JSONには記載不足をオフラインでも分析できるよう、Issue本文も収録します。

本文の先頭には完全合成データ宣言を置き、合成モデル`SIM-TV-A`、合成FW`SIM-FW-A.1`、合成証跡ID`SYNTH-EV-NNN`を記載します。

## kind別の本文見出し

### `kind:bug` / `kind:question`

次の見出しを使用します。記載がない場合や`未記載`とある場合は、Browser Use実習における情報不足の判定対象です。

- `事象`
- `再現手順`
- `期待結果`
- `実際結果`
- `証跡`

### `kind:test-gap`

不具合報告ではないため、情報不足の判定対象にはしません。次の見出しを使用します。

- `確認したい観点`
- `現在のテスト`
- `追加案`
- `期待する成果`

## ラベル

1件のIssueに、原則として各分類から1個ずつ付けます。

### 種類

- `kind:bug`: 不具合候補
- `kind:test-gap`: テスト観点の追加候補
- `kind:question`: 追加確認が必要な問い合わせ

### 対象領域

- `area:power`
- `area:update`
- `area:hdmi`
- `area:network`
- `area:ui`
- `area:audio`
- `area:accessibility`

### 重要度

- `severity:S1`: 基本機能が利用できない重大な事象
- `severity:S2`: 主要機能への大きな影響
- `severity:S3`: 回避可能な機能影響
- `severity:S4`: 軽微な表示・改善候補

この重要度定義も教材用の架空ルールです。実在する組織の基準ではありません。

### 状況

- `status:needs-info`: 情報不足
- `status:investigating`: 確認中
- `status:retest`: 再確認待ち
- `status:resolved`: 教材上の確認完了

## 作成予定のGitHubラベル

| ラベル | 色 |
|---|---|
| `kind:bug` | `d73a4a` |
| `kind:test-gap` | `0e8a16` |
| `kind:question` | `d876e3` |
| `area:power` | `5319e7` |
| `area:update` | `1d76db` |
| `area:hdmi` | `0052cc` |
| `area:network` | `006b75` |
| `area:ui` | `bfdadc` |
| `area:audio` | `fbca04` |
| `area:accessibility` | `c5def5` |
| `severity:S1` | `b60205` |
| `severity:S2` | `d93f0b` |
| `severity:S3` | `fbca04` |
| `severity:S4` | `0e8a16` |
| `status:needs-info` | `fef2c0` |
| `status:investigating` | `c2e0c6` |
| `status:retest` | `1d76db` |
| `status:resolved` | `6f42c1` |

## 公開前チェック

- READMEに「すべて架空」と明示されている
- 氏名、メールアドレス、企業名、取引先名を含まない
- 実製品名、実機ID、実ファームウェア番号を含まない
- 社内URL、認証情報、実ログ、実画面を含まない
- 原本、CSV、JSONのID・タイトル・状態・ラベルが一致する
- Closed予定のIssueは、登録後にGitHub上でもClosedへ変更する
- タイトルは`[SYNTH][LAB-TV-NNN]`で始まる
- 外部URL、添付、Assignee、Milestoneを設定しない
- 講師用の正解表を公開リポジトリに置かない
