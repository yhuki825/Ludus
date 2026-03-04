# Ludus株式会社 コーポレートサイト

## ファイル構成

```
ludus-website/
├── index.html    # メインページ
├── _headers      # Cloudflare Pages セキュリティヘッダー設定
├── _redirects    # Cloudflare Pages リダイレクト設定
└── README.md     # 本ファイル
```

## Cloudflare Pages へのデプロイ手順

### 方法 1: ドラッグ＆ドロップ（最も簡単）

1. [Cloudflare Dashboard](https://dash.cloudflare.com/) にログイン
2. **Workers & Pages** → **Create application** → **Pages** タブを選択
3. **Upload assets** を選択し、`ludus-website` フォルダをそのままドラッグ＆ドロップ
4. プロジェクト名を入力して **Deploy site** をクリック

### 方法 2: Git 連携（推奨）

1. このフォルダを GitHub / GitLab リポジトリにプッシュ
2. Cloudflare Dashboard → **Workers & Pages** → **Create application** → **Pages**
3. **Connect to Git** でリポジトリを連携
4. ビルド設定は不要（静的 HTML のため）
5. **Save and Deploy** をクリック

## 注意事項

- `_headers` ファイルにより、セキュリティヘッダーが自動的に付与されます。
- `_redirects` ファイルは SPA フォールバック用です（静的サイトでも念のため同梱）。
- 外部リソース（Google Fonts, Tailwind CDN, Lucide Icons, Unsplash 画像）を使用しているため、インターネット接続が必要です。
