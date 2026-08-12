# 公開テレビ検証教材

AIによるBrowser Use / Computer Useを安全に練習するための公開教材です。

## 公開情報について

このリポジトリの会社名、製品、画面、事象、Issue、日時、識別子は、すべて教材用に作成した架空の情報です。実在する個人・企業・取引先・製品とは関係ありません。

次の情報は登録しません。

- 氏名、メールアドレス、アカウント名などの個人情報
- 企業名、取引先名、部署名、案件名
- 実製品名、実機ID、シリアル番号
- 実際のファームウェア番号、社内URL、認証情報
- 実画面の画像、実ログ、社内文書からの引用

教材へ情報を追加するときは、必ず架空情報だけを使用してください。

## 教材の内容

- [Issue一覧](../../issues): Browser Useで読む20件の公開Issue
- [Browser Use実習](prompts/browser-task.md): GitHubを根拠付きで読む課題
- [Computer Use実習](prompts/computer-task.md): 表計算アプリを操作する課題
- [CSVスナップショット](data/issues_snapshot.csv): 表計算実習と取得不能時の予備データ
- [JSONスナップショット](data/issues_snapshot.json): 全Issue本文を含むBrowser Useの予備データ
- [Issueデータ仕様](specs/issue-schema.md): 項目・ラベル・公開前チェック
- `dataset/issues.yml`: 20件のIssue原本

## 想定する使い方

GitHubアカウントを持たない受講者は、公開Issueの閲覧、検索、ラベルによる絞り込み、CSV/JSONのダウンロードを行えます。Issueの作成、編集、コメントにはGitHubへのログインが必要です。

## データ利用上の注意

このデータは研修・動作確認専用です。実際の品質判断、製品評価、障害傾向の分析には使用できません。

講師用の正解表は公開リポジトリには置きません。
