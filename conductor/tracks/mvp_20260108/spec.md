# Track Spec: Build the core MVP of habit-heat

## 1. 概要
「habit-heat」の最小機能セット（MVP）を構築する。ユーザーがタスクを管理でき、その成果がGitHub風のヒートマップ（Heat Graph）に反映されるWebアプリケーションを実現する。

## 2. 技術要件
- **Frontend:** Angular + Ignite UI for Angular (OSS)
- **Backend:** Hono on Cloudflare Workers
- **Database:** Cloudflare D1
- **Styling:** Ignite UI components with soft & minimal theme

## 3. スコープ
- **プロジェクト初期構築:** Angular, Hono, pnpm, Cloudflareの統合設定。
- **タスク管理:**
  - タスクの作成、読み取り、更新（完了/未完了）、削除。
  - D1への永続化。
- **Heat Graph UI:**
  - 過去1年間の日次タスク完了状況の表示。
  - カラーマッピング: 完了数に応じて色が暖色系（薄い黄色 -> オレンジ -> 赤）に変化。
- **ストリーク計算:** 現在の連続達成日数を表示。

## 4. 非機能要件
- **パフォーマンス:** 軽量なバンドルサイズと高速なエッジ実行。
- **レスポンシブ:** モバイルおよびデスクトップブラウザへの対応。
- **ミニマリズム:** シンプルで直感的なUI。
