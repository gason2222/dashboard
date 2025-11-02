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
│   ├── history-image2diary.json        # Image2Diaryの更新履歴
│   └── history-recipe-from-fridge.json # Recipe from Fridgeの更新履歴
└── README.md              # このファイル
```

## 更新履歴の追加方法

各アプリごとに個別の更新履歴ファイルを編集します。

### ファイル構成

各アプリごとに `update-history/history-{アプリID}.json` というファイルを作成・編集します。

- `history-image2diary.json` - Image2Diaryの更新履歴
- `history-recipe-from-fridge.json` - Recipe from Fridgeの更新履歴

### JSONファイルの形式

```json
[
  {
    "date": "2025-11-02",
    "update-history": "更新内容をここに記述"
  },
  {
    "date": "2025-10-22",
    "update-history": "別の更新内容"
  }
]
```

### 追加手順

1. 対応するアプリのJSONファイルを開く
   - Image2Diary → `update-history/history-image2diary.json`
   - Recipe from Fridge → `update-history/history-recipe-from-fridge.json`
2. 配列の先頭に新しい更新履歴オブジェクトを追加
3. 日付は `yyyy-mm-dd` 形式で記入
4. `update-history` に更新内容を記述
5. 保存してコミット・プッシュ

### 新しいアプリを追加する場合

1. `update-history/history-{アプリID}.json` ファイルを作成
2. 上記のJSON形式で更新履歴を記述
3. HTMLのアプリカードに `data-app="{アプリID}"` 属性を設定
4. ID属性を `latest-date-{アプリID}`, `latest-content-{アプリID}`, `history-list-{アプリID}` に設定

**注意**: 
- 各アプリの最新の更新履歴が「アプリを開く」ボタンの下に表示されます
- マウスホバー（またはタップ）で過去10件の履歴がモーダルで表示されます
- 日付順に自動ソートされます（新しい順）
- ファイルが存在しない、または読み込みエラーの場合、そのアプリの更新履歴エリアは非表示になります

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

