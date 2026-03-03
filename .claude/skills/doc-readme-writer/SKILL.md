---
name: readme-writer
description: プロジェクトの README.md を作成する。PRDとDESIGNからセットアップ手順、コマンド一覧、技術スタックを含む README を生成する。ユーザーが「README を作って」「セットアップ手順」「/doc:readme」と言ったときに使用する。
---

# README Writer

PRD と DESIGN を入力として、clone してすぐ動かせる README を作成する。

## 前提条件

docs/PRD.md と docs/DESIGN.md が存在すること。

## 作成手順:

1. PRD からプロダクト概要を取得
2. DESIGN から技術スタックとコマンドを取得
3. package.json 等から実際に使えるスクリプトを確認
4. assets/template.md のテンプレートに従って作成
5. プロジェクトルートに README.md を保存

## ルール:

- 5ステップ以内で動く手順にする
- 環境変数は .env.example を参照させる（値は書かない）
- Scripts には実際に存在するコマンドだけ載せる
- docs/ 内の各ドキュメントへのリンクを含める
