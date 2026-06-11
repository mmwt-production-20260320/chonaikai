# 〇〇町内会 ホームページ

## 📁 ファイル構成

```
chonaikai/
├── index.html        ← トップページ（お知らせ）
├── events.html       ← イベント情報ページ
├── css/
│   └── style.css     ← デザイン設定
├── js/
│   └── main.js       ← 動作スクリプト
├── images/           ← 写真を入れるフォルダ
└── README.md         ← このファイル
```

---

## 🚀 GitHub Pages で公開する手順

### 1. GitHubにリポジトリを作る
1. GitHub（https://github.com）にログイン
2. 右上の「＋」→「New repository」をクリック
3. リポジトリ名を `chonaikai` にする（なんでもOK）
4. 「Public」を選択（無料公開に必要）
5. 「Create repository」をクリック

### 2. ファイルをアップロードする
1. 作ったリポジトリのページを開く
2. 「uploading an existing file」をクリック
3. このフォルダの中のファイルをすべてドラッグ＆ドロップ
   - ⚠️ フォルダごとでなく、**css・js・imagesフォルダの中身も含めて** 構造を保ってアップロード
4. 「Commit changes」をクリック

### 3. GitHub Pages を有効にする
1. リポジトリの「Settings」タブを開く
2. 左メニューの「Pages」をクリック
3. Source を「Deploy from a branch」に変更
4. Branch を「main」、フォルダを「/ (root)」に設定
5. 「Save」をクリック

### 4. 公開URLを確認する
数分後に `https://あなたのGitHubユーザー名.github.io/chonaikai/` で公開されます！

---

## ✏️ サイトの更新方法

### ◆ お知らせを追加する（index.html）

`index.html` を開いて、`★ここにお知らせを追加していきます★` のコメント直後に以下をコピーして追加：

```html
<article class="news-item">
  <time class="news-date" datetime="2025-MM-DD">2025年〇月〇日</time>
  <span class="news-tag tag-info">お知らせ</span>
  <h3 class="news-headline">
    <a href="#">タイトルをここに書く</a>
  </h3>
  <p class="news-body">
    内容をここに書きます。
  </p>
</article>
```

**タグの種類：**
- `tag-important` → 赤：重要なお知らせ
- `tag-event`     → 緑：イベント関連
- `tag-info`      → 紺：一般的なお知らせ

### ◆ イベントを追加する（events.html）

`events.html` の `★ここにイベントを追加していきます★` の後にコピーして追加：

```html
<article class="event-card">
  <div class="event-date-block">
    <span class="event-month">〇月</span>
    <span class="event-day">〇</span>
    <span class="event-year">2025</span>
  </div>
  <div class="event-body">
    <h3 class="event-title">イベント名</h3>
    <ul class="event-meta">
      <li>🕒 時間</li>
      <li>📍 場所</li>
    </ul>
    <p class="event-desc">内容説明</p>
  </div>
</article>
```

### ◆ 写真を追加する

1. `images/` フォルダに写真ファイル（例：`natsu2025.jpg`）を入れる
2. `events.html` の該当イベント内の以下のコメントを外す：
   ```html
   <img src="images/natsu2025.jpg" alt="夏祭りの様子" class="event-photo">
   ```
3. またはギャラリーに追加：
   ```html
   <figure class="gallery-item">
     <img src="images/photo01.jpg" alt="写真の説明">
     <figcaption>2025年 夏祭り</figcaption>
   </figure>
   ```

### ◆ 変更をGitHubに反映する

1. GitHubのリポジトリページを開く
2. 変更したファイル（例：`index.html`）をクリック
3. 鉛筆アイコン（Edit）をクリックして直接編集 → 「Commit changes」
   
   **または**
   
   ファイルをドラッグ＆ドロップで上書きアップロード

---

## 🔧 カスタマイズ方法

### 町内会名を変える
`index.html` と `events.html` の `〇〇町内会` を実際の名前に変える

### メールアドレスを変える
`index.html` と `events.html` の `chonaikai@example.com` を実際のアドレスに変える

### 家紋マークを変える
`css/style.css` の `.kamon` に好きな文字や絵文字を使えます（例：`🏠` `🌸` `🎋`）

---

## 💡 VSコードを使った方が便利な点

GitHub上で直接編集もできますが、VSコードを使うと：
- 複数ファイルを同時に管理できる
- 保存前にプレビュー確認ができる（Live Serverプラグイン）
- ファイルをまとめてドラッグ＆ドロップできる

どちらでも更新できます！

---

*作成：Claude (Anthropic)*
