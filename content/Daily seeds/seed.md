---
title: 更新のやり方(個人用)
description: 日々の日記です。
tags:
    - setting
    - Quartz
---

## 使い方(完全個人用)

作業フォルダは ~/Documents/gh-pages のみ。

## 編集 → 確認 → 公開 の流れ（毎回これ）
① Markdown を編集してから

cd ~/Documents/gh-pages

 content/ 以下の .md を編集

② ローカルで確認

npx quartz build --serve

これで、
http://localhost:8080
にアクセスして 数式 / 画像 / graph を確認。

※ node_modules が無ければ、bashで

npm ci

を実行。

③ 公開するときは

git add .

git commit -m "Update notes"

git push

👉 これだけで GitHub Actions が自動デプロイ

👉 数分後に
https://saku0903hu.github.io/
 に反映

## 🚫 やらなくていいこと

public/ を git 管理する

node_modules/ を push する

Pages の Branch 設定を触る

npm run build を手で公開用に回す

Actions が全部やる。

## 🧹 整理
my-quartz を消すなら
rm -rf ~/Documents/my-quartz

ローカルを軽くする
rm -rf node_modules public


（必要になったら npm ci で復活）

## 🔧 次にやると楽になるカスタム（おすすめ順）

1️⃣ トップページを MOC にする
content/index.md を「研究ノート入口」に

2️⃣ Graph View を主役にする
Obsidian Publish っぽさMAX

3️⃣ PDF / 元LaTeXをリンク
assets/pdf/anyon_theory.pdf とか

4️⃣ private ノートの分離

content_private/   ← git 管理しない

## 最後に確認

https://saku0903hu.github.io/
👉 いま見えてる？

anyon のページで
👉 数式・画像・分割はOK？
