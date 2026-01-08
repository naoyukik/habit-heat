# Track Plan: Build the core MVP of habit-heat

## Phase 1: プロジェクト基盤構築
- [ ] Task: モノレポ構成のセットアップ
    - [ ] Subtask: ルートディレクトリに `pnpm-workspace.yaml` を作成（frontend, backendを指定）
    - [ ] Subtask: `.gitignore` を更新し、各ディレクトリの依存関係などを適切に除外
- [ ] Task: フロントエンドの初期セットアップ (Angular + Ignite UI)
    - [ ] Subtask: `frontend/` ディレクトリにAngularプロジェクトを作成 (Angular CLI または Analog)
    - [ ] Subtask: Ignite UI for Angular (OSS) を `frontend/` にインストール・設定
    - [ ] Subtask: `frontend/` 用のCloudflare Pages デプロイ設定を追加
- [ ] Task: バックエンドの初期セットアップ (Hono + Cloudflare Workers)
    - [ ] Subtask: `backend/` ディレクトリにHonoプロジェクトを作成
    - [ ] Subtask: `backend/` 用のCloudflare Workers デプロイ設定
    - [ ] Subtask: HonoとAngularのAPI通信確認（Hello World）
- [ ] Task: データベース設定 (Cloudflare D1 + Drizzle)
    - [ ] Subtask: D1 データベースの作成とバインディング設定
    - [ ] Subtask: Drizzle ORM のセットアップとスキーマ定義（Tasksテーブル）
    - [ ] Subtask: マイグレーションスクリプトの作成と実行
- [ ] Task: Conductor - ユーザーマニュアル検証 'Phase 1: プロジェクト基盤構築' (Protocol in workflow.md)

## Phase 2: タスク管理APIの実装
- [ ] Task: タスク作成API (POST /tasks)
    - [ ] Subtask: テスト作成: タスク作成エンドポイントの結合テスト
    - [ ] Subtask: 実装: D1へのタスク挿入処理
- [ ] Task: タスク一覧取得API (GET /tasks)
    - [ ] Subtask: テスト作成: タスク一覧取得の結合テスト
    - [ ] Subtask: 実装: D1からの全件取得処理
- [ ] Task: タスク状態更新API (PUT /tasks/:id)
    - [ ] Subtask: テスト作成: タスク完了状態更新の結合テスト
    - [ ] Subtask: 実装: ID指定による完了フラグのトグル処理
- [ ] Task: タスク削除API (DELETE /tasks/:id)
    - [ ] Subtask: テスト作成: タスク削除の結合テスト
    - [ ] Subtask: 実装: ID指定による削除処理
- [ ] Task: Conductor - ユーザーマニュアル検証 'Phase 2: タスク管理APIの実装' (Protocol in workflow.md)

## Phase 3: フロントエンド実装 (タスク管理)
- [ ] Task: タスク一覧・追加UI実装
    - [ ] Subtask: テスト作成: タスクリストコンポーネントの単体テスト
    - [ ] Subtask: 実装: Ignite UIのリストコンポーネントを使用した表示
    - [ ] Subtask: 実装: 入力フォームと追加機能
- [ ] Task: タスク操作UI実装
    - [ ] Subtask: テスト作成: タスク完了・削除インタラクションのテスト
    - [ ] Subtask: 実装: チェックボックスによる完了状態変更とAPI連携
    - [ ] Subtask: 実装: 削除ボタンとAPI連携
- [ ] Task: Conductor - ユーザーマニュアル検証 'Phase 3: フロントエンド実装 (タスク管理)' (Protocol in workflow.md)

## Phase 4: Heat Graph & ストリーク実装
- [ ] Task: 活動履歴API (GET /stats)
    - [ ] Subtask: テスト作成: 日次完了数集計ロジックのテスト
    - [ ] Subtask: 実装: D1から日付ごとの完了タスク数を集計して返すAPI
- [ ] Task: Heat Graph コンポーネント実装
    - [ ] Subtask: テスト作成: データに基づいて色が変化するロジックのテスト
    - [ ] Subtask: 実装: グリッド表示と活動量に応じた暖色系カラーマッピング
- [ ] Task: ストリーク計算・表示
    - [ ] Subtask: テスト作成: 連続達成日数の計算ロジックテスト
    - [ ] Subtask: 実装: 現在のストリーク数をUIに表示
- [ ] Task: Conductor - ユーザーマニュアル検証 'Phase 4: Heat Graph & ストリーク実装' (Protocol in workflow.md)
