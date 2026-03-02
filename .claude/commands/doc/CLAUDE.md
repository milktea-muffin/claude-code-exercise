# ドキュメント作成コマンド

MVP 開発に必要なドキュメントを作成するコマンド群。
必ず以下の順番で実行すること。各コマンドは前のドキュメントを参照する。

## 実行順序

1. `/doc:prd` — 要件定義書（docs/PRD.md）
2. `/doc:design` — 技術設計書（docs/DESIGN.md）← PRD を参照
3. `/doc:tasks` — タスク分解（docs/TASKS.md）← PRD + DESIGN を参照
4. `/doc:readme` — README（README.md）← PRD + DESIGN を参照

## ルール

- 前のドキュメントが存在しない場合は、先に作成するよう案内する
- 各ドキュメントは docs/ ディレクトリに保存する（README.md のみルート）
- 作成後は必ずセルフレビューを行う