# 技術設計書（DESIGN.md）作成

docs/PRD.md を読み込み、技術設計書を作成する。
$ARGUMENTS に追加の技術的制約や好みがあればそれも考慮する。

design-writer スキルを参照し、assets/template.md のテンプレートと
references/example.md の見本に従って docs/DESIGN.md を作成する。

## 前提条件

docs/PRD.md が存在すること。なければ「先に /doc:prd で PRD を作成してください」と案内する。

## 手順

1. docs/PRD.md を読み込む
1. 未確定の技術判断があればまとめて1回で質問する
1. design-writer スキルの手順に従って設計書を作成する
1. PRD との整合性をチェックする
1. docs/DESIGN.md に保存する
1. 「次は /doc:tasks でタスク分解できます」と案内する