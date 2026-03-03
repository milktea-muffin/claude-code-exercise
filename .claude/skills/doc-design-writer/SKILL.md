---
name: design-writer
description: 技術設計書（DESIGN.md）を作成する。PRDからDB設計、API設計、技術スタック選定を含む統合設計書を生成する。ユーザーが「技術設計」「DESIGN.md を作って」「アーキテクチャ」「どう作るか」「/doc:design」と言ったときに使用する。また、実装中にAPI、DBスキーマ、セキュリティに関するコードを書く際にも自動参照される。
---

# Design Writer

PRD を入力として、技術設計+DB設計+API設計+セキュリティを1ファイルに統合した MVP 向け設計書を作成する。

## 前提条件

docs/PRD.md が存在すること。

## 作成手順

1. docs/PRD.md を読み込み、MVP 機能・画面・制約を把握する
2. 未確定の技術判断はまとめて1回で質問する
3. assets/template.md のテンプレート構造に従って作成する
4. references/example.md を参考に粒度を合わせる

## 各セクションの作成ルール

- Tech Stack - 各レイヤーに技術と選定理由を明記。理由は「なぜこれを選び他を選ばなかったか」を含める
- Architecture - システム構成図はASCII。ディレクトリ構成はツリーで各ディレクトリに1行説明。データフローを矢印で示す
- DB Schema - ER図はMermaid erDiagramで書く（必須）。テーブル定義はカラム名、型、NULL可否、デフォルト、説明を含める
- API Endpoints - PRDのMVP機能ごとにエンドポイントを設計。主要エンドポイントにRequest/ResponseのJSON例を付ける
- Security Checklist - チェックリスト形式。認証、認可、入力バリデーション、XSS、CSRF、Rate Limitを最低限含める
- Key Decisions - 判断、選択した技術、理由、却下した候補をテーブルで記録

## 整合性チェック（作成後に自動確認）

- PRD の全 MVP 機能に対応する API エンドポイントがあるか
- PRD の全画面に対応するルートがあるか
- DB テーブル間のリレーションに矛盾がないか

## 実装フェーズでの参照ルール（このスキルは実装中も自動参照される）

- API 実装時は定義されたパス、メソッド、レスポンス形式に従う
- DB 変更時は先に DESIGN.md を更新してから実装する
- 定義にないエンドポイント追加時は先に DESIGN.md を更新する
- 変更があれば Key Decisions に理由を追記する