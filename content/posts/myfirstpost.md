---
title: "Hugoでホームページを新しくしてみた"
date: 2021-05-04T12:31:53+09:00
draft: false
isCJKLanguage: true
tags: [
    "",
]
---

これまで使っていた（使ってない）ホームページは、Academicテーマを色だけカスタマイズしたものだった。また、どこかのサイトに従ってGitHub Actionでの自動デプロイをしてみたが、正直なにがどうなっているのかも分からなかったので、etchテーマをカスタマイズして作り直すことにした。

### テーマのカスタマイズ
etchテーマは素の状態だとポストしたもののリストがトップに出てくるだけなので、Academicっぽく上のほうに自己紹介、下に論文やらなんやらのリストを表示する形にしたい。layouts/index.htmlを見てみると、layouts/partial/hogehoge.htmlとしてそれぞれのパーツを置いておいてそれを呼び出している形だったので、about.htmlとpapers.html等々を新たに作成して追加した。
htmlとかcssとか触ったことがない人間なのでabout.htmlとかはよくわからないまま無理やり書いてみた。アイコン間のスペースのあけ方とか、
```html
            </div>&nbsp;&nbsp;&nbsp;
```
ってしていてもう絶対にお作法と違う。

### GitHub Pages action
ビルドとデプロイはGitHub Pages actionを用いて自動化した。
https://qiita.com/peaceiris/items/d401f2e5724fdcb0759d  
このページを参考にして、gh-pages.ymlを追加。mainブランチからgh-pagesブランチへデプロイしている。
以下のyamlファイルをデフォルトブランチの.github/workflows/gh-pages.ymlとしてpushしたらサイトが無事公開された。

```yml
name: Hugo

on: push

jobs:
  gh-pages:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
        #with:
          #submodules: true

      # https://github.com/marketplace/actions/github-pages-action
      - name: Setup
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: latest
          extended: true

      - name: Build
        run: hugo --minify

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_branch: gh-pages
```

### 疲れました
testtest
{{< alert color="success" >}}
alertのテストです
{{< /alert >}}