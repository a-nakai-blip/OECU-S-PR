# OECU-S-PR

大阪電気通信大学 スポーツ科学専攻向けの広報投稿支援Webアプリです。Google Apps Script (GAS) で動作します。

## v0.6
- Anthropic Claude APIへ移行
- 写真の画像入力に対応
- イベント名がある場合はClaude Web Searchで公式情報を確認
- Instagram / X / OECU JOURNAL向け原稿生成
- OECU JOURNAL原稿を `kouhou@osakac.ac.jp` へGmail送信
- Google Sheets投稿履歴・Google Drive作業ファイル
- X投稿の基本実装
- Instagram直接投稿は画像公開の運用承認まで無効

## GAS設定
Script Properties:
- `ANTHROPIC_API_KEY`（必須）
- `CLAUDE_MODEL=claude-sonnet-5-5`
- `ALLOWED_DOMAIN=osakac.ac.jp`
- `HISTORY_SHEET_ID`（setupProjectで自動作成）
- `UPLOAD_FOLDER_ID`（setupProjectで自動作成）

OpenAI版から移行する場合、既存のSheets/Driveはそのまま利用できます。v0.6では `OPENAI_API_KEY` は使用しません。

## セキュリティ
APIキーはGitHubへコミットせず、Apps ScriptのScript Propertiesに保存してください。
