# GitHub Pages 設定手順

## ✅ 完了した作業

1. ✅ ファイルの作成とコミット
2. ✅ GitHubへのプッシュ（mainブランチ）

## 📋 GitHub Pages の有効化手順

### 1. GitHubリポジトリページにアクセス
https://github.com/gason2222/dashboard にアクセスしてください。

### 2. Settings（設定）を開く
- リポジトリページの上部メニューから「**Settings**」をクリック

### 3. Pages セクションを開く
- 左側のメニューから「**Pages**」をクリック（「Code and automation」セクション内）

### 4. ソースを設定
- 「**Source**」セクションで「**Deploy from a branch**」を選択
- 「**Branch**」で「**main**」を選択
- 「**/ (root)**」を選択（デフォルト）
- 「**Save**」ボタンをクリック

### 5. デプロイ完了まで待つ
- 通常、1-2分程度でデプロイが完了します
- 完了すると、以下のURLでアクセス可能になります：
  ```
  https://gason2222.github.io/dashboard/
  ```

### 6. カスタムドメイン（任意）
- カスタムドメインを使いたい場合は、「**Custom domain**」欄に入力
- 設定すると、DNS設定が必要になります

## 🔄 更新方法

ファイルを更新する場合は、以下のコマンドを実行：

```bash
git add .
git commit -m "Update: 変更内容を記述"
git push origin main
```

プッシュ後、数分でGitHub Pagesに反映されます。

## 📝 注意事項

- 画像ファイル（`images/image2diary.png`、`images/recipe-from-fridge.png`）は後で追加できます
- 画像を追加したら、同じようにコミット・プッシュしてください
- 初回のデプロイには数分かかる場合があります

## ✨ 次のステップ

1. GitHub Pagesを有効化（上記の手順1-5）
2. デプロイ完了後、URLにアクセスして動作確認
3. 必要に応じて画像ファイルを追加

