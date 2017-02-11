---
layout: post
title: "リアルもくもく『JAWS-UG金沢 第15回 もくもく会』に参加"
date: 2016-10-24 14:34:49 +0900
comments: true
published: true
categories: JAWS-UG AWS
---

2016-10-22に [JAWS Festa 東海道 2016 ｜ JAWS-UG](https://jaws-ug.jp/es/jaws-festa-toukaido-2016/) に参加できなかったので [JAWS-UG金沢 第15回 もくもく会 - JAWS-UG 金沢 | Doorkeeper](https://jawsug-kanazawa.doorkeeper.jp/events/52936) に参加した。

ITビジネスプラザ武蔵の部屋に2人きりという残念な集客ぷりでしたが、おかげで次回以降のネタ出しなどをできてよかった。次は流行りのサーバレスやろうと思いますのでみんなきてね。11/25(金)です。よろしくお願いします。

結局仕事を進めたのだが、 AWS の API Gateway からなんと SDK がダウンロードできるというのを初めて知った! これを使う iOS アプリがビルドできないというところでタイムアップ。Xcode(Objective-C) と cocoapods と AWS SDK という3本同時学びはよくない。いちいち動作がわからん。とりあえず AWS のヘルプを見ると [API Gateway で API の SDK を生成する - Amazon API Gateway](https://docs.aws.amazon.com/ja_jp/apigateway/latest/developerguide/how-to-generate-sdk.html#how-to-generate-sdk-ios) といううち、 Xcode に直接ライブラリをインストールする手法が乗っているのでこちらからやっていこう。

明日は金沢マラソンということもあって、本日は懇親会なしで解散しました。

