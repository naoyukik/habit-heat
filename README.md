# habit-heat

GitHub風の「草（Heat Graph）」が生える習慣管理ツール。
タスクを完了するたびにグラフが「熱を帯びる（Heat up）」視覚的体験を提供し、モチベーション維持をサポートします。

## 概要

- **シンプルタスク管理**: 日々のタスクを簡単に登録・消化。
- **Heat Graph**: 活動量に応じて色が変化するヒートマップで継続を可視化。
- **ストリーク**: 連続達成日数をカウント。

## 技術スタック

- **Frontend**: Angular + Ignite UI for Angular
- **Backend**: Hono on Cloudflare Workers
- **Database**: Cloudflare D1 (SQLite)
- **Deployment**: Cloudflare Pages & Workers

## 開発状況

現在、初期セットアップとMVP（Minimum Viable Product）の計画策定が完了し、開発フェーズに移行しています。
詳細は `conductor/` ディレクトリ内のドキュメントを参照してください。
