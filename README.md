# SleepTrace

スマートバンドの睡眠計測データを記録・可視化するWebアプリケーションです。

## デモ

- **フロントエンド**: https://sleeptrace-frontend.pages.dev
- **バックエンド API**: https://sleeptrace-backend.yshimura1001.workers.dev

### ゲストログイン
```
ユーザー名: guest
パスワード: Bc@r1#DMXn
```

## 主な機能

- 睡眠データの登録・編集・削除
- ダッシュボードでの統計情報表示（平均値、トレンド分析）
- 週間データのグラフ表示
- 睡眠分析（トレンドライン付きチャート）
- CSVインポート/エクスポート
- JWT認証によるユーザー管理
- ダークモード対応

## リポジトリ
- **フロントエンド**: https://github.com/yshimura1001/sleeptrace-fontend
- **バックエンド**: https://github.com/yshimura1001/sleeptrace-backend

## 技術スタック

### フロントエンド

| カテゴリ | 技術 |
|---------|------|
| フレームワーク | Vue.js 3.5 (Composition API) |
| 言語 | TypeScript 5.9 |
| ビルドツール | Vite 7 |
| 状態管理 | Pinia |
| ルーティング | Vue Router |
| スタイリング | Tailwind CSS 3.4 |
| UIコンポーネント | shadcn/ui (Radix Vue / Reka UI) |
| グラフ描画 | Chart.js + vue-chartjs |
| ホスティング | Cloudflare Pages |

### バックエンド

| カテゴリ | 技術 |
|---------|------|
| フレームワーク | Hono 4.11 |
| 言語 | TypeScript |
| バリデーション | Zod |
| 認証 | JWT (hono/jwt) |
| ホスティング | Cloudflare Workers |

### データベース

| カテゴリ | 技術 |
|---------|------|
| データベース | Cloudflare D1 (SQLite) |

## アーキテクチャ

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Vue.js SPA    │────▶│   Hono API      │────▶│  Cloudflare D1  │
│ Cloudflare Pages│     │ Cloudflare Workers│    │    (SQLite)     │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

## ローカル開発
| カテゴリ | 技術 |
|---------|------|
| メインOS | Windows 11 Pro |
| サブOS | Ubuntu 24.04.03(WSL)|
| エディタ | VS Code, Antigravity|
| AIコーディングエージェント | Calude(Code), Gemini(AI Pro)|

### 前提条件
- Node.js 24.13.0
- pnpm

### セットアップ

```bash
# フロントエンド
cd sleeptrace-frontend
pnpm install
pnpm dev

# バックエンド
cd sleeptrace-backend
npm install
npm run dev
```

## デプロイ

```bash
# フロントエンド
cd sleeptrace-frontend
pnpm run deploy

# バックエンド
cd sleeptrace-backend
npm run deploy
```
