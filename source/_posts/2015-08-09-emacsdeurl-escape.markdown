---
layout: post
title: "emacsでurl escape"
date: 2015-08-09 16:45:53 +0900
comments: true
categories: emacs
---

safariのURLをコピーすると、URLエンコードされておらず

`https://ja.wikipedia.org/wiki/ごいた`

このようになってしまうのだが、本来欲しいのは以下のような形である。

`https://ja.wikipedia.org/wiki/%E3%81%94%E3%81%84%E3%81%9F`

このコンバートを支援してくれる、

http://blog.koshigoe.jp/archives/2006/02/emacs_html_1.html

を導入した。このあたりからemacs list hack できるようになっていきたいものである。
最近、init.elでerrorを吐くことがあって、`(setq debug-on-error t)` を仕掛けたら、
止まりまくりと気づいたのでなんとかしたいなぁーと思っていたので、このあたりの
シンプルなものから手をつけていきたい。

そもそもチュートリアルすらやってないのがいかんか。

(おっと、octopressが賢いのかhttps文字列をちゃんと検出してちゃんとエスケープしてくれた。)
