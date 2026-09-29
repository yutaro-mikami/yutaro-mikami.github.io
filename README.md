# Homepage maintenance guide

This proposal keeps the existing public URLs but separates content from layout.
GitHub Pages can build this repository with Jekyll.

## 日常的に触る場所

### 所属・メール・研究紹介
`_data/profile.yml` だけを編集します。

### 論文・プレプリント
`_data/publications.yml` だけを編集します。

- `status: published` → Papers / 論文（出版済み）
- `status: preprint` → Preprints / プレプリント

番号は自動で振られます。

### CV
`cv.pdf` を同じ名前で置き換えます。

### 論文コメント
`_paper_comments/` の Markdown ファイルを編集します。
新しいものを追加するときは既存ファイルを複製して本文を書き換えます。

- `listed: true` → hidden.html の一覧に出す
- `listed: false` → ページは残すが一覧には出さない

### クラシックのレビュー
`_music_reviews/` の Markdown ファイルを編集します。
`classic/main.html` の一覧は自動生成されます。

### アニメ等
`anime/main.md` を編集します。

## スマホからの更新

GitHub のWeb画面で対象ファイルを開き、Edit（鉛筆アイコン）→ Commit changes で更新できます。
普段は HTML や CSS を触る必要はありません。

## hidden ページについて

`hidden.html` とそこから辿れるページには `noindex,nofollow` を付けていますが、これはアクセス制限ではありません。
URLを知っている人は閲覧できます。本当に非公開にしたい内容には使わないでください。

## 現行版から直した点

- 英日トップページのCSS重複を解消
- 論文リストを1ファイルに集約
- hidden / paper comment / classical music の一覧を自動生成
- `cv.pdf` / `CV.pdf` の大文字小文字問題を解消
- `anime/main.html` と Pollini ページの誤った `<title>` を修正
- 各趣味ページに共通CSSを適用
- `.DS_Store` と `texput.log` は移行対象から除外
