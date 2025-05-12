# 企業ユーザー管理システム

役割ベースのアクセス制御を備えた、企業およびユーザーの管理を行うフルスタックアプリケーションです。

## 技術スタック

- **フロントエンド**：Next.js 14（TypeScript、Tailwind CSS、App Router）
- **バックエンド**：Express.js
- **データベース**：MySQL

## 主な機能

- ユーザー認証機能（新規登録、ログイン、パスワード再設定）
- 役割ベースのアクセス制御（管理者、企業マネージャー、一般メンバー）
- 企業情報の管理（作成・取得・更新・削除）
- ユーザー情報の管理（作成・取得・更新・削除）
- レスポンシブ対応デザイン
- アバター画像のファイルアップロード

## プロジェクト構成

```
.
├── frontend/               # Next.js フロントエンドアプリケーション
└── backend/               # Express.js バックエンドアプリケーション
```

## セットアップ手順

### 前提条件

- Node.js 18+
- MySQL 8+
- npm or yarn

### フロントエンドのセットアップ

1. フロントエンドディレクトリへ移動：
```bash
cd frontend
```

2. 依存パッケージをインストール：
```bash
npm install
```

3. `.env.local` ファイルを作成し、以下を記述：
```
NEXT_PUBLIC_API_URL=http://localhost:5000
```

4. 開発サーバーを起動：
```bash
npm run dev
```

### バックエンドのセットアップ

1. バックエンドディレクトリへ移動：
```bash
cd backend
```

2. 依存パッケージをインストール：
```bash
npm install
```

3. `.env` ファイルを作成し、以下を記述：
```
PORT=5000
DB_HOST=localhost
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=company_management
JWT_SECRET=your_jwt_secret
```

4. 開発サーバーを起動：
```bash
npm run dev
```

## データベースの準備

1. `company_management` という名前のMySQLデータベースを作成してください。
2. バックエンドを起動することで、必要なテーブルが自動で作成されます。

## APIエンドポイント一覧

### 認証関連

- POST /api/auth/register
- POST /api/auth/login
- POST /api/auth/forgot-password
- GET /api/auth/me

### 企業関連

- GET /api/companies
- POST /api/companies
- PUT /api/companies/:id
- DELETE /api/companies/:id

### ユーザー関連

- GET /api/users
- POST /api/users
- PUT /api/users/:id
- DELETE /api/users/:id

## ライセンス

MIT
