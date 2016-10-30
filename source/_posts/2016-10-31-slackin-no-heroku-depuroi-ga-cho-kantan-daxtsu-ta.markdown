---
layout: post
title: "slackin の Heroku デプロイが超簡単だった"
date: 2016-10-31 01:33:39 +0900
comments: true
published: true
categories: 
---

みんなステキでイケてる slack を使いたい。けれども、無料で使ってる限り(?)はメールアドレス指定の招待制となってしまう。オープンな議論や進行をしたいのに、ここがクローズになってしまうのは残念だよなあ。

というのはみんな思ってるらしく、招待権限を持ったユーザーによるAPIで招待してくれるウェブアプリを構築してくれるものがあった。

[rauchg/slackin: Public Slack organizations made easy](https://github.com/rauchg/slackin)

これである。 Kanazawa.rb でやってたのを見て私もやってみた。超簡単だった。その GitHub 上の 表示されている `README.md` のドキュメントから Heroku に飛べばOK。

`SLACK_CHANNELS` という環境変数は空欄じゃないとダメらしい。ここにだけハマったがあとは本当にポチポチコピペとかするだけで簡単にできた。

そういうわけでできたのがこれ

[Join ha4go-mokumoku on Slack!](https://ha4go-mokumoku-inviter.herokuapp.com/)

毎月やってる [ha4go もくもく会](http://ha4go-mokumoku.yaranaika.me/) 向けなので、ぜひ参加してほしい。11月の募集要項は [ha4go オンライン もくもく会 2nd - connpass](http://connpass.com/event/42982/) で公開している。

