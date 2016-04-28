---
layout: post
title: "RailsアプリのMySQLをmuninで見るようにした"
date: 2016-04-29 00:08:46 +0900
comments: true
published: true
categories: qiita
---

Qiita書いた。

[Docker上のMySQL稼働情報をmuninで見る - Qiita](http://qiita.com/PharaohKJ/items/c1606c5420ddef564a2e)

とりあえず、今やってる `CakePHP + MySQL` のプロジェクトと、 `Ruby on Rails + MySQL` のプロジェクトで差異とか、負荷との関係とか、いろいろ知見が得られたらいいなと思って入れました。

さすがにこういう運用しないと見えてこないもの、の、アナライザは早く仕込むに越したことは無いよね。

- 楽に
- 正確に
- アプリ自体のジャマをせず
- 他との関係が見やすい

というのが重要な要素かな？まぁ `munin` はこれに属すると思うが、 `zabbix` はなんでもできる感じだった。ああ、本当は

- ヤバイときは通知がくる

のが大事なんだが `munin` はあるのかな？アラートメールぐらいはあるか。

最近のzabbixは試してないが、いまのところ **楽さ** では munin が圧勝している・・・はず・・・。あ、それも docker で各サービスあげるようにしたらまた力関係がかわってくるかも。そういえば、昔 zabbix で トップページを毎分 curl して応答時間を縦軸にとって横軸時間でどんなグラフになるか見てたような気が。そういうのできるのかな。
