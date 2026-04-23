# Focus Mode

ADHDのエンジニア向けAI搭載タスク管理アプリ

## 機能

- AIがタスクの優先度を判定し、今やるべき1つを選んでくれる
- 「後でやる」で指定時刻に自動復活
- AIが状況に応じたアクションを提案
- カレンダーでタスクの期限・復活予定を一覧

## デプロイ手順

### 1. このリポジトリをGitHubにプッシュ

```bash
git init
git add .
git commit -m "initial commit"
git remote add origin https://github.com/YOUR_USERNAME/focus-mode.git
git push -u origin main
```

### 2. Vercelにデプロイ

1. [Vercel](https://vercel.com) にGitHubアカウントでログイン
2. 「Add New → Project」をクリック
3. `focus-mode` リポジトリを選択して「Import」
4. 「Environment Variables」で以下を追加:
   - Key: `ANTHROPIC_API_KEY`
   - Value: AnthropicのAPIキー
5. 「Deploy」をクリック

### 3. 完了

発行されたURL（例: `https://focus-mode-xxx.vercel.app`）にアクセスしてください。

スマホのホーム画面に追加すると、アプリのように使えます。

## ファイル構成

```
focus-mode/
├── public/
│   └── index.html    ← フロントエンド
├── api/
│   └── chat.js       ← Anthropic API中継（APIキーを隠す）
├── package.json
└── README.md
```
