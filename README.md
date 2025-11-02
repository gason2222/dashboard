# WEBアプリ総合案内ページ

柔らかく優しいデザインの総合案内ページです。

## 画像の配置方法

以下の画像ファイルを `images` フォルダに配置してください：

- `images/image2diary.png` - Image2Diaryのスクリーンショット
- `images/recipe-from-fridge.png` - Recipe from Fridgeのスクリーンショット

## ファイル構成

```
dashboard/
├── index.html              # メインのHTMLファイル
├── manifest.json           # PWA設定ファイル
├── images/                 # 画像ファイルを配置するフォルダ
│   ├── image2diary.png
│   └── recipe-from-fridge.png
├── update-history/          # 更新履歴JSONファイル
│   └── history.json        # 更新履歴データ
└── README.md              # このファイル
```

## 更新履歴の追加方法

`update-history/history.json` ファイルを編集して更新履歴を追加できます。

### JSONファイルの形式

```json
[
  {
    "date": "2025-01-15",
    "update-history": "更新内容をここに記述"
  },
  {
    "date": "2025-01-14",
    "update-history": "別の更新内容"
  }
]
```

### 追加手順

1. `update-history/history.json` を開く
2. 配列の先頭に新しい更新履歴オブジェクトを追加
3. 日付は `yyyy-mm-dd` 形式で記入
4. 保存してコミット・プッシュ

**注意**: 
- 最新の更新履歴が各アプリカードの「アプリを開く」ボタンの下に表示されます
- マウスホバー（またはタップ）で過去10件の履歴がモーダルで表示されます
- 日付順に自動ソートされます（新しい順）

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

**GitHub Pages（現在使用中）**
- GitHubリポジトリがあれば自動でホスティング
- 無料でシンプル
- `Settings` > `Pages` で有効化
- 詳細な設定手順は `GITHUB_PAGES_SETUP.md` を参照

**Firebase Hosting**
- Googleのサービス
- 高速で信頼性が高い
- CLIで簡単デプロイ

