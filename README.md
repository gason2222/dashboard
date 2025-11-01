# WEBアプリ総合案内ページ

柔らかく優しいデザインの総合案内ページです。

## 画像の配置方法

以下の画像ファイルを `images` フォルダに配置してください：

- `images/image2diary.png` - Image2Diaryのスクリーンショット
- `images/recipe-from-fridge.png` - Recipe from Fridgeのスクリーンショット

## ファイル構成

```
dashboard/
├── index.html          # メインのHTMLファイル
├── images/             # 画像ファイルを配置するフォルダ
│   ├── image2diary.png
│   └── recipe-from-fridge.png
└── README.md          # このファイル
```

## ホスティング方法

静的ファイルのみなので、以下の無料ホスティングサービスが利用可能です：

### おすすめ：Vercel

**理由：**
- GitHubと連携可能で自動デプロイ
- 高速で無料
- カスタムドメイン対応
- 使いやすい管理画面

**デプロイ手順：**

1. **GitHubにリポジトリを作成**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/your-username/dashboard.git
   git push -u origin main
   ```

2. **Vercelでデプロイ**
   - https://vercel.com にアクセス
   - 「Sign Up」でGitHubアカウントでログイン
   - 「Add New Project」をクリック
   - 先ほど作成したリポジトリを選択
   - 「Deploy」をクリック
   - 数秒でデプロイ完了！

### その他の選択肢

**Netlify**
- GitHub連携可能
- ドラッグ&ドロップでもデプロイ可能
- https://www.netlify.com

**GitHub Pages**
- GitHubリポジトリがあれば自動でホスティング
- 無料でシンプル
- `Settings` > `Pages` で有効化

**Firebase Hosting**
- Googleのサービス
- 高速で信頼性が高い
- CLIで簡単デプロイ

