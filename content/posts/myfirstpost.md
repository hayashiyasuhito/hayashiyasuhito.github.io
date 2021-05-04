---
title: "Myfirstpost"
date: 2021-05-04T12:31:53+09:00
draft: false
isCJKLanguage: true
tags: [
    "",
---
### Hugoテーマの変更
これまで使っていたホームページは、テーマの中で何が行われていたかも、git hub actionsで何が起こっているかもよくわからないけどとりあえず動いているという状況でした。
なんとなく気持ち悪かったので、シンプルなテーマを探してきて自分でいろいろカスタマイズしてみようと思い、etchテーマをいじった結果が現状です。

### GitHub Pages action
ビルドとデプロイはGitHub Pages actionを用いて自動化しているので、確認など必要ないpostsやpapers、awardsなどの更新はhugoが動かせない環境でも行えるようになりました。
https://qiita.com/peaceiris/items/d401f2e5724fdcb0759d  
このページを参考にして、gh-pages.ymlを追加。mainブランチからgh-pagesブランチへデプロイしています。etchはSCSSを使うテーマだったらしく(よくわかっていない)、Setup Hugoにextended: trueを追加しました。
