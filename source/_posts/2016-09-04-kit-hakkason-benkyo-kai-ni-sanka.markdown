---
layout: post
title: "『KITハッカソン勉強会』に参加"
date: 2016-09-04 05:33:15 +0900
comments: true
published: true
categories: 
---

2016-09-03 Sat に[KITハッカソン勉強会(KIT, さくらクラウド, PFU 共催) - KIT ハッカソン | Doorkeeper](https://kithackation.doorkeeper.jp/events/51290) に参加した。

サブタイトルは「IoT ハッカソン、MQTT (および、そのセキュリティ)について考える」ではあったが、結局は「ガッツリさくらインターネットさまのハンズオンをやった」 & 「RabbitMQのチュートリアルをやって機能を学ぶ」という感じの内容であった。

## 私の狙い

- pomo のアップグレード
- pomo on ラズパイの完成
- 上記を通じて AWS IoT MQTT がラズパイ上でできることを確認
- そのセキュリティモデルを説明できるようになっておく
- MQTTの事例を皆様と共有し、踏まえてどうするべきかを考える

## 結果

pomo、ラズパイ、AWS IoT はほとんど触れず。結局 MQTT の事例をお話しただけ。MQTTハンズオンも、まぁもう1万回はみた & やったであろう RabbitMQ チュートリアルだったので LT 資料をまとめていてしまった。

さくらインターネットさんのクラウドハンズオンがよくて(というか、今まで [ha4go](https://kanazawa.ha4go.net/) とかで使ってたけど、チュートリアルすらまともによまずに徒手空拳でやってた)、ついていった。

内容としては、まずグローバルからつながるサーバを1台たて、それをGatewayにしたサーバを1台たて、スイッチでつなげるというもの。あとDocker、composeもやった(さすが前佛さんやで)。

ハッキリいって、既存のIaaSでやりたいことはこれでほとんどできるな。ファイアウォールルールぐらいまで行って欲しかったがまぁメンツ的に無理であろう。会終了後に「こんなんでサーバできます。っていうの、学生がいきなりやると、何が便利なのかさっぱりわからず、伝わらず、おっさんだけが『便利だろ？どやぁ？』ってことになってんじゃないかなぁ」と感じた。

「MQTTを運用に使ってる人は挙手！」 → 挙手なし。この情報も収穫だったかもしれない。

## 反省

### ラズパイのモビリティをあげる

自宅では DHCP で MAC みて固定でいろいろ払い出ししているが、外部に持ちだした時

- 無線LANの設定を注入する方法
- 注入した結果、俺はここだとディスカバリする方法

を確立させておかないと、セットアップしてる間に1時間はすぎる。次はなんとかしたい。

あっ、あと、ずっと自分のをラズパイ2あたりだと思ってたのに「うおっ、ラズパイ初代久しぶりにみました」みたいなこと言われてビビる。そしてちゃんと初代だった。


### どうして巨大なインスタンス1台ではダメか? を説明できなかった

これについては先日の AWS 勉強会で自分がまとめたくせに、そういう質問が飛んだ時に「え? 多いほうがいいのは当たり前じゃん?」という気持ちになってしまったが、Docker や クラスタ管理ツールの台頭する意味など、正しく説明できなかったのはよくない。


### MQTT、及びその実装のセキュリティモデルを説明できない

「MQTT over TLS」「AWS IoT の認証モデル」などをざくっと概要しか知らず、セキュリティセキュリティ言われて自分のなかで落とし込めてん買ったなと反省。まともな議論になった場合、ついていけなかったであろう。まぁ今回はほんとなんかよくわからないとてもそこまでいく感じはなかった。よくわからない、というのは、何を議論したいのかわからんという感じ。机の上に乗る資料、現実の抱える問題が足りなかったんじゃないか。

## 資料

- [wslash/zabbix3](https://github.com/wslash/zabbix3)
- [MQTTプロジェクト - PukiWiki Plus!](http://www.kitnet.org/hackathon/index.php?MQTT%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88)

## 夕食

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BJ5Ed-Ggf2x/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">Lジャンジャン？</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した写真 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-09-03T11:14:33+00:00">2016 9月 3 4:14午前 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
