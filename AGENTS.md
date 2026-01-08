# AI Agent Guidelines - habit-heat

このドキュメントは、本プロジェクト「habit-heat」に携わるすべてのAIエージェントが遵守すべき開発指針とコンテキストをまとめたものである。

## 1. プロジェクトの概要
- **製品名:** habit-heat
- **ビジョン:** タスク完了によってGitHub風のグラフが「熱を帯びる（暖色系に変化する）」視覚的体験を通じた習慣管理。
- **デザイン哲学:** ソフト & ミニマル。ノイズを排し、ユーザーの活動（Heat Graph）を主役とする。

## 2. 技術スタック
エージェントは以下の技術スタックに基づいたコード生成および提案を行うこと。
- **Frontend:** Angular (TypeScript), Ignite UI for Angular (OSS)
- **Backend:** Hono (TypeScript), Cloudflare Workers
- **Database:** Cloudflare D1 (SQLite), Drizzle ORM
- **Package Manager:** pnpm
- **Infrastructure:** Cloudflare Pages / Workers

## 3. 開発運用ルール
- **言語:** `conductor/` 内の全ドキュメント（spec, plan等）および `AGENTS.md` は**日本語**で記述する。
- **ブランチ戦略:** トランクベース開発に近い運用。
  - `main`: プロダクション。
  - `track-id`: トラック単位の作業ブランチ（例: `mvp_20260108`）。プレフィックス（feature/等）は不要。
- **コミット:** 各タスク完了ごとにコミットし、Git Notesを使用してタスクサマリーを記録する（デフォルト設定）。
- **テスト:** テスト駆動開発（TDD）を推奨。機能実装前にテストコードを提示・作成すること。

## 4. コーディングスタイル
`conductor/code_styleguides/` 配下の各ガイドラインを最優先で参照すること。
- `general.md`: 一般原則
- `typescript.md`: TypeScript規約
- `angular.md` (あれば): Angular固有規約
- `html-css.md`: マークアップおよびスタイル規約

## 5. Conductor メソドロジー
本プロジェクトは Conductor メソドロジーに従って管理されている。
- `conductor/tracks.md`: 全トラックの一覧。
- `conductor/tracks/<track_id>/plan.md`: 現在の実行計画。
- 実装を開始する際は必ず `plan.md` の現在のステップを確認し、完了後にチェックを入れること。
