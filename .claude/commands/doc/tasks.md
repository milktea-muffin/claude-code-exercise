# タスク分解（TASKS.md）作成

docs/PRD.md と docs/DESIGN.md を読み込み、実装タスクに分解する。
$ARGUMENTS に追加の制約があればそれも考慮する。

task-planner スキルを参照し、assets/template.md のテンプレートに従って
docs/TASKS.md を作成する。

## 前提条件

docs/PRD.md と docs/DESIGN.md が存在すること。なければ先に作成するよう案内する。

## 手順

1. PRD から機能一覧とマイルストーンを読み込む
1. DESIGN から技術スタック、DB、API を読み込む
1. task-planner スキルの手順に従ってタスクを分解する
1. 依存関係とクリティカルパスを確認する
1. docs/TASKS.md に保存する
1. 「最初のタスクから実装を始められます」と案内する