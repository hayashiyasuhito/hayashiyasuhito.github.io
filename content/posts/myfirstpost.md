---
title: "Myfirstpost"
date: 2021-05-04T12:31:53+09:00
draft: false
isCJKLanguage: true
tags: [
    "",
]
---

### Hugoテーマの変更
これまで使っていたホームページは、テーマの中で何が行われていたかも、git hub actionsで何が起こっているかもよくわからないけどとりあえず動いているという状況でした。
なんとなく気持ち悪かったので、シンプルなテーマを探してきて自分でいろいろカスタマイズしてみようと思い、etchテーマをいじった結果が現状です。

### GitHub Pages action
ビルドとデプロイはGitHub Pages actionを用いて自動化しているので、確認など必要ないpostsやpapers、awardsなどの更新はhugoが動かせない環境でも行えるようになりました。  
https://qiita.com/peaceiris/items/d401f2e5724fdcb0759d  
このページを参考にして、gh-pages.ymlを追加。mainブランチからgh-pagesブランチへデプロイしています。etchはSCSSを使うテーマだったらしく(よくわかっていない)、Setup Hugoにextended: trueを追加しました。
 現場水温からポテンシャル水温の換算式は、ここ。

　塩分とは、海水1kg中に溶解している全固形物質のg数。ただし、これを計測することは困難なので、電気 伝導度を計測し、標準海水(一本5000円くらいで売っている)が示す伝導度との比で決定する。比なので、塩分は、原則、無単位。でもややこしいので、 psu(practical salinity unit; 実用塩分単位)を付けることがある。海水の塩分は0-35psu程度で変化する。

　海水密度は、水温と塩分、そして圧力を用いて状態方程式で計算する。
### 疲れました
testtest
