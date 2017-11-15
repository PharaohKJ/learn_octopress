---
layout: post
title: "Mashup Awardsにアイデアだけ参加して予選敗退した"
date: 2017-11-15 17:59:42 +0900
comments: true
published: true
categories: Hackathon
---

2017-10-21（土）、『KANAZAWAオープンイノベーションハッカソンMashup Awards 2017 金沢予選』に参加した。

いろいろあって初日21日の夕方までの参加になってしまったんだが、アイデアは得票することができて、男子率100％プログラマー率100％という最強のチームができあがった。

そもそも『独り言が多い日は調子がいいのか、それとも、悪いのか』を知りたいと常日頃思っていた。それには独り言の録音が必要だし内容の解析もやりたくなる。加えて、私は他人…いや存在しない誰かに説明しようとしたりツイートしようとしたりして日本語化・アウトプットしていく過程でいろいろ気づいていくタイプなので、積極的に独り言をしたいのである。

そういうわけでまとまったアイデアがこちら。

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:35.55555555555556% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/Bafqh2jhan2/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">9票獲得しました！</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)がシェアした投稿 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-10-21T03:20:34+00:00">2017 10月 20 8:20午後 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

総括すると、なんだかんだで当日できること調査するってのは後手後手だし、できることから要求を考えないと全然欲しいものと違うものができちゃったなという印象。それでもオチは悪くはなかった。やっぱハッカソンは勝てないなあ。

初日に手分けしていろいろ妥協して実装に至った流れは以下。

## 入力
感情認識ヒューマノイドロボットである[Pepper (ロボット) - Wikipedia](https://ja.wikipedia.org/wiki/Pepper_(%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88))を用いる。本来は常に聴いてストリーム処理してほしかったんだがいきなりしゃべりかけても各動作のトリガーは引けないらしい。そのため、独り言というよりはペッパーくんに語りかけるという仕様になった。


## 分析
ペッパーくんの顔を見ないと感情は認識できないらしく、ペッパーくんの方を向いて話さないといけないらしい。私が求めていたのは語調で感情を認識してもらいたかったのだ。真にやりたかったのは「つらい♪」というと「つらくなさそう」「つらい！」というと「つらそう」と記録されることだ。だいぶ独り言とは遠くなってきた。

語調がダメならしょうがないので日本語から分析してもらおう。これには[Text Analytics API | Microsoft Azure](https://azure.microsoft.com/ja-jp/services/cognitive-services/text-analytics/)を用いることにした。


## データ保存場所
[mBaaSでサーバー開発不要！ | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/) を用いた。APIキーの発行だけでサクサク使えてとてもよかった。イベントスクリプトも実行できるので、このデータ保存をトリガーして出力部を叩こう！　と思ったらこの保存をトリガーしたイベントスクリプトは設定できないとのこと。しょうがないのでペッパーくん側で分析と出力を行うようにした。


## 出力
感情カレンダービューはサーバが要るし、作ってる時間も間に合わななそうだ。LINEさんもいらっしゃっていたのでLINEを用いることにした。あんまり？　人気ないが実はLINEにはTwitterと同じように自分のタイムラインがあるのだ。そこに感情をポストすることで自分の感情の変化を記録できるからよかろう。

と考えてたんだがタイムラインAPIがないらしい。しょうがないのでグループチャットにした。これまた独り言とは遠くなってきた。


## 結果として

結果としてペッパー君と会話=独り言しているとLINEのグループチャットに感情分析が投稿されたり腹減り度が投稿されたりするので、そのグループチャット参加者は「メシに誘い出そう！」とか「今は期限悪いから話かけないほうがいいな」とか判断できて業務を円滑に進むことができる。

というものになった。動いてるところ動画とプレゼンシートをLINEでもらって確認したが悪くなった。が予選敗退してしまった。

