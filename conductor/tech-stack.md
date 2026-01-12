# 技術スタック - habit-heat

## 1. フロントエンド

- **フレームワーク:** Angular
- **言語:** TypeScript
- **UIライブラリ:** Ignite UI for Angular (OSS version)
- **状態管理:** Angular Signals / RxJS (Standard)
- **パッケージマネージャー:** pnpm

## 2. バックエンド (API)

- **フレームワーク:** Hono
- **言語:** TypeScript
- **ランタイム:** Cloudflare Workers

## 3. データベース & ストレージ

- **データベース:** Cloudflare D1 (SQLite on the edge)
- **ORM:** Drizzle ORM

## 4. インフラ & デプロイ

- **プラットフォーム:** Cloudflare Pages (Frontend) & Cloudflare Workers (API)
- **CI/CD:** GitHub Actions (Automated deployment to Cloudflare)
