# README.md 作成

docs/PRD.md と docs/DESIGN.md を読み込み、README.md を作成する。

## 前提条件

docs/PRD.md と docs/DESIGN.md が存在すること。
加えて package.json 等のプロジェクト設定ファイルが存在すればそれも参照する。

## 手順

### Step 1: 情報収集

以下を読み込む:
- docs/PRD.md（プロダクト概要）
- docs/DESIGN.md（技術スタック、コマンド）
- package.json / pyproject.toml / go.mod 等（利用可能なスクリプト）
- .env.example（必要な環境変数）

### Step 2: README.md 作成

プロジェクトルートに README.md を保存する。

構成:
1. **プロジェクト名 + 1行説明**
2. **Setup** - Prerequisites（必要なランタイムとバージョン）、セットアップ手順（5ステップ以内で動く状態に）
3. **Scripts** - テーブル: コマンド / 説明（実際に使えるコマンドのみ）
4. **Tech Stack** - 使用技術を1行ずつ
5. **Docs** - docs/ 内の各ドキュメントへのリンク

ルール:
- clone してから最短で動く手順を書く
- 環境変数は .env.example を参照させる（値は書かない）
- 実際に存在するコマンドだけ Scripts に載せる

最後に「README.md を作成しました」と報告する。