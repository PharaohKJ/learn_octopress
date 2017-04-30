---
layout: post
title: "ADO.NET Entity Framework入門をはじめた"
date: 2017-04-30 18:06:48 +0900
comments: true
published: true
categories: .NET 勉強会
---

JAZUG北陸もくもく会に参加し、もう7年前の記事だが以下の第1回の4.まで進めた。コンソールアプリからはじめさえてもらえるところにシンプルさを感じてこれを選んだが、もっといい教材があれば教えて欲しい。

最終的なゴールは "TypeScript + AngularJS" + "ASP.NET + SQL Server" + "on Azure" のプロダクトを動かすとしている。

[連載：ADO.NET Entity Framework入門 － ＠IT](http://www.atmarkit.co.jp/fdotnet/ef4basic/index/index.html)

[4月30日野々市交友舎でAzureもくもく勉強会してますが、良かったら来ませんか？ - connpass](https://jazug-hokuriku.connpass.com/event/54479/)

Visual Studio 2017 Community Editionだが愛するMySQLWorkbenchのような手軽さでテーブル1つ作成することがさくっとできてよかった。

しかし最近はRailsのようにマイグレーションコードを書かないとピンとこないようになってしまった。

ローカルのSQL Serverはすでに動かしているんだけれど、接続先ダイアログに指定する文字列がピンとこなかったが、「Windowsキー > SQL」と入力したらでてくるマネージャを起動したらそれっぽい文字列があったのでそれを採用することでDBの作成と接続ができたようだ。

さてじゃあ次はDBをバージョンアップしたらそれの適用とかどうやってくれるんだろう？　うまいことやってくれるのか、はたまたしくじってリバートするときはどうやったら戻ってくれるんだろうなど思うところあれどいったんこの入門をやってみることにする。

Ruby on Railsも手に吸い付いてきたなと思ったのは「何かあったときにちゃんと巻き戻せる、やりなおせるようになったとき」だったので、きっとこれも製品の実装を進めていけば哲学も含む理解が深まると期待している。

あとTOREZOについて少しプレゼンし少しアンケートをとったが、やはりなかなかガチの.NETサーバ案件というのは転がってなさそうだ。JAVAは結構あるようなんだが。ライセンスフィーの問題なんだろうか？　Visual Studio使ってWindowsアプリ作ってますというようなエンジニアが素直に移行すればもっとそういう案件あると思うんだが。

やはりみんなライセンスフィー、サーバのお値段などで私と同じようにOSSのほうに行ってしまったというのが現実なのであろうか。そういえば日本だけは異常にサーバーサイドWindowsの採用率が低いというのを伺ったことがあるな。

[日本でのApache比率は高すぎないかい？！ - Nothing ventured, nothing gained.](http://takoratta.hatenablog.com/entry/20060625/1151249406)

2006-06-25！　なんと10年も前の話だった！　しかも単に日経に乗っている会社のウェブページがかえすサーババージョンを見ているだけか。

最近の動向じゃIISが伸びてるらしい。

[Microsoft IIS、Apache抜いて1位に返り咲き - 7月Webサーバ調査 | マイナビニュース](http://news.mynavi.jp/news/2016/07/21/054/)

nginxはだいぶ哲学的にIISやApacheと違うと思うんだがそれは私の思い込みなのか？
