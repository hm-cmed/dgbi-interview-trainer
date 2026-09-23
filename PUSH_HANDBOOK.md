# GitHub へ push して公開する手順

このフォルダはそのまま GitHub リポジトリになります。以下のいずれかの方法で公開できます。

---

## 方法A：GitHub CLI（`gh`）が入っている場合（最短）

フォルダ内で以下を実行します（`YOURNAME` は自分の GitHub ユーザー名など任意のリポジトリ名に変えてください）。

```bash
cd dgbi-interview-trainer
git init
git add .
git commit -m "DGBI interview trainer (self-scored offline edition)"
gh repo create dgbi-interview-trainer --public --source=. --push
```

その後、GitHub のリポジトリ画面で **Settings → Pages → Build and deployment → Source** を **GitHub Actions** に設定します。数十秒後に公開 URL が表示されます。

---

## 方法B：ブラウザだけで（CLI 不要）

1. GitHub で新規リポジトリを作成（例：`dgbi-interview-trainer`、Public）。README等は追加しない。
2. 作成後の画面の「uploading an existing file」から、このフォルダの中身
   （`index.html` / `README.md` / `LICENSE` / `.nojekyll` / `.github/`）をドラッグ＆ドロップしてコミット。
   - `.github` フォルダはドラッグでフォルダごと上げれば階層が保たれます。うまくいかない場合は `index.html` だけでも公開できます（自動デプロイなしの方法C参照）。
3. **Settings → Pages → Source** を **GitHub Actions** に設定。

---

## 方法C：Actions を使わず branch から直接公開（最もシンプル）

`index.html` と `.nojekyll` さえ置けば動きます。

1. リポジトリに `index.html` と `.nojekyll` を置く（`.github/` は無くてよい）。
2. **Settings → Pages → Source** を **Deploy from a branch** にし、**Branch: main / (root)** を選んで Save。
3. 1〜2 分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

---

## 既存リポジトリに追加する場合

リモートを手動で設定する形：

```bash
cd dgbi-interview-trainer
git init
git add .
git commit -m "Add DGBI interview trainer"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```

---

## 確認

公開後、スマホと PC の両方で URL を開き、ケース切り替え・チェック・採点・進捗保存（再読み込みしても Lv が残る）が動くか確認してください。うまく表示されない場合は数分待つ（初回ビルドに時間がかかることがあります）か、`.nojekyll` がリポジトリ直下にあるか確認してください。
