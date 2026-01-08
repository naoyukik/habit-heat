# Tech Stack - habit-heat

## 1. Frontend
- **Framework:** Angular
- **Language:** TypeScript
- **UI Library:** Ignite UI for Angular (OSS version)
- **State Management:** Angular Signals / RxJS (Standard)
- **Package Manager:** pnpm

## 2. Backend (API)
- **Framework:** Hono
- **Language:** TypeScript
- **Runtime:** Cloudflare Workers

## 3. Database & Storage
- **Database:** Cloudflare D1 (SQLite on the edge)
- **ORM:** Drizzle ORM

## 4. Infrastructure & Deployment
- **Platform:** Cloudflare Pages (Frontend) & Cloudflare Workers (API)
- **CI/CD:** GitHub Actions (Automated deployment to Cloudflare)
