---
layout: post
title: "災害支援時における行政と民間の関係はどうあるべきか『JAWS DAYS 2017』に参加した"
date: 2017-03-24 08:45:27 +0900
comments: true
published: true
categories: AWS jaws-ug
---

[JAWS DAYS 2017 | JAWS-UG主催の最大のイベント「JAWS DAYS 2017」は「Link Up - JAWS-UGで新しい世界とつながる一日」をテーマに2017年3/11(土)にTOC五反田メッセ(東京)にて開催](http://jawsdays2017.jaws-ug.jp/)

に参加した。当日を時系列で。

## 分煙ならぬ分納豆ルームを作って欲しい（イチャモン）

とりあえずパワーをつけるためにホテルで朝食を。めずらしくバイキングスタイルじゃない！　すごーい！

洋食をお願いして食堂に充満する腐臭。バイキングスタイルじゃないのに取り放題状態となっている納豆パックがセルフサービスドリンクのとなりに置いてある。

納豆は体にいいのかもしれないけれど、本当に勘弁してほしい。むずかしいな。

## 会場へ

会場はちょうどアマゾンウェブサービスさんのある目黒と五反田駅の間ぐらいの [TOC GOTANDA MESSE](http://messe.toc.co.jp/) というところ。ちょうど町並みを歩くことができてよかった。途中気になる店の写真がこちら。


<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/bzNvQfr4xb">pic.twitter.com/bzNvQfr4xb</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840341277891682304">2017年3月10日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

これは噂をおうかがいしたことのある二郎インスパイア系だ。さすがに朝からはやってない。夜ワンチャン？　と考えたが休みの日の夜はやってなかった！

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/F3oCb3hCjY">pic.twitter.com/F3oCb3hCjY</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840342537726386176">2017年3月10日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

そもそも焼肉店にソロで行くことに抵抗がある人は孤独のグルメを見ろ！　きっとこの店に食事されてる方はみんな発電所に違いない。「ひとり」を強調するのいいね。


## 会場入り


### インスタンスタグをつけるスタート

さて、本日はいくつかボランティアスタッフとしてお手伝いすることになっていた。まずは自分にインスタンスタグをつけることから。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/Q32VuIXxi0">pic.twitter.com/Q32VuIXxi0</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840356034543734784">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

こういうのはコミュ障の私には非常に助かる。そういうわけで「遠征中です」「話しかけてOK」なんかをつけてみた。


### AWSかるた（物理）のお手伝い

まずはAWSかるた（物理）のお手伝いをはじめた。アイコンをみて何サービスか覚えるのがちょっと楽しいし、アイコンデザインもサービスを知っていると「うーん深い」と勝手に思えてきたり「えっ？　なんで？」と思えたりとても楽しいのでオススメ。データは [jaws-ug/assets: 画像などの素材公開用リポジトリです](https://github.com/jaws-ug/assets) とかにあるらしい。

AWSはとにかくサービスがめちゃくちゃ増える！　用意するのは大変だあ。


## 一発目 『JAWS-UG meets Windows ～Windows開発者およびインフラエンジニアのためのDev&Ops on AWS～ 渡邉源太 / 福井厚』

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">これから参戦 <a href="https://t.co/eQFohWKjsD">pic.twitter.com/eQFohWKjsD</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840366172675559424">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

[JAWS-UG Meets Windows (JAWS Days 2017)](https://www.slideshare.net/AmazonWebServicesJapan/jawsug-meets-windows-jaws-days-2017)

加藤家家訓として「専用道具を使え」というのが教えになっている。どのぐらい染み込んでいるのかというと、ある日マイブラザーから電話があって「兄貴！　家にケーブルテレビ引いたんでCATV対応って書いてあるLANケーブル買ってきて全部変えたわ！」というぐらいに染み込んでいるのである。

そういうわけでサーバのOSにWindowsを選択しないという状況において、道具としてWindowsを用いてはならぬ。と考えていたのだが、最近.NET系の開発環境がOSSの方向に舵が切られているのが明確だし、むしろこれでWindowsエンジニア勢と話が通じないのはまずいと常日頃思っていたので参加した。

- Run Command はエージェントレスなのか質問したかったがちょっと時間足りなかった。
- AWS Tools for Wondows PowerShell そういうのもあるのか。
- 今の lambda (C#)は Amazon Linux + .NET core らしい。


## 二発目『Docker on Elastic Beanstalk 〜明日から本番で使えるかも〜 子安 輝』

[Docker on Elastic Beanstalk 〜明日から本番で使えるかも〜 | セッション | JAWS DAYS 2017](http://jawsdays2017.jaws-ug.jp/session/1797/)

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/EZ3UrSkQgO">pic.twitter.com/EZ3UrSkQgO</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840386894844256256">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

[巨人の肩の上 - Wikipedia](https://ja.wikipedia.org/wiki/%E5%B7%A8%E4%BA%BA%E3%81%AE%E8%82%A9%E3%81%AE%E4%B8%8A)

以下引用。正直「虎の威を借る狐」のようなネガティブな比喩だと勝手に思っていたが、実はこんなステキな比喩だとは思わなかった。

> 「巨人の肩の上にのる矮人」（きょじんのかたのうえにのるわいじん、ラテン語: nani gigantum umeris insidentes）という言葉は、西洋のメタファーであり、現代の解釈では、先人の積み重ねた発見に基づいて何かを発見することを指す。

- passenger-docker ! そういうのもあるのか。
- awsebが動かないでまともなハンズオンにならなかった…。マイMBPのPython実行環境がめちゃくちゃだとわかった。


## 弁当箱回収

昼食が無料でくばられたのでそれのゴミを回収する手伝いをした。こういうお仕事でもいろいろ得られるものはあるねえ。物理大量になると突然スケールするのが難しくなるのはなんでもだな…。私はフィッシュフライ弁当をいただいた。うまい。


## JAWS-UGブースに立つ

ソロで立つのはツライなーと思っていたが石川出身で今は都内に勤務されている方が手伝ってくれた！　よかった。

さすがにセッション中は来客がほとんどなかったが、セッションとセッションの間には何人かいらっしゃった。結局答えた内容としては「関東ではいろいろ分科があるが、地方はもう実質初心者だろうが誰でもウェルカムです」という一点のみであった。はっはっは。

あらかじめ答える内容を用意しておいたほうがよいかもしれない…。特にそのUGアピール内容などあるでしょうし。


## 三発目『Amazon Kinesis Analyticsを触ってみよう 高田雅人』

[Amazon Kinesis Analyticsを触ってみよう | セッション | JAWS DAYS 2017](http://jawsdays2017.jaws-ug.jp/session/1525/)

そもそもKinesisってなんだよ、何が有利なんだよってところから入ったんだけれど「ためて」「読んで」「あれこれする」んじゃなくて、ストリームであれこれするということ。上記からいける資料を読んでなんとなくわかった。

そしてその分析をみんな大好きSQLで処理できてしまうというのがAnalyticsらしい。なるほど！


## 四発目『東日本大震災を経験した私達が後世に残す物資支援の仕組み「必要な人に必要な支援を必要な分だけ」 矢崎 淳一』 & 『熊本震災時におけるクラウド活用について 渡邉一弘 / 富山孝治』

[東日本大震災を経験した私達が後世に残す物資支援の仕組み「必要な人に必要な支援を必要な分だけ」 | セッション | JAWS DAYS 2017](http://jawsdays2017.jaws-ug.jp/session/1271/)

[熊本震災時におけるクラウド活用について | セッション | JAWS DAYS 2017](http://jawsdays2017.jaws-ug.jp/session/1656/)

3.11時においてJAWS勢は多大な貢献をした、というのはちょうどそのときに「東京リージョン」が開設されたのもあって、いろいろ伝説として伺っている。なんのこっちゃ？　という方はぜひ『G-CLOUD Magazine 2011 Summer』を読んでいただきたい。ずばり「特集1　真価を発揮！　AWS　ディザスタリカバリとクラウド」である。

<a href="https://www.amazon.co.jp/G-CLOUD-Magazine-2011-Summer-%E7%B7%A8%E9%9B%86%E9%83%A8/dp/4774147206/ref=as_li_ss_il?ie=UTF8&qid=1490314856&sr=8-4&keywords=g+cloud+magazine&linkCode=li2&tag=pharaohkj-22&linkId=91ae99423c92d14b9434f603e75c0632" target="_blank"><img border="0" src="//ws-fe.amazon-adsystem.com/widgets/q?_encoding=UTF8&ASIN=4774147206&Format=_SL160_&ID=AsinImage&MarketPlace=JP&ServiceVersion=20070822&WS=1&tag=pharaohkj-22" ></a><img src="https://ir-jp.amazon-adsystem.com/e/ir?t=pharaohkj-22&l=li2&o=9&a=4774147206" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />

PDF版もこちらで買える > [G-CLOUD Magazine 2011 Summer | Gihyo Digital Publishing … 技術評論社の電子書籍](https://gihyo.jp/dp/ebook/2011/978-4-7741-4720-8)

目次を上記サイトより引用しておく。

```
特集1
進化を発揮！AWS
ディザスタリカバリとクラウド

第1章：Amazon Web Services最新動向［2011春・夏］……片山暁雄
第2章：DR［ディザスタリカバリ］のためのクラウド
第1部：cloudpackにおけるAWSによるDR……鈴木宏康
第2部：CloudworksにおけるDR……大石良
コラム：AWS―UGの東日本大震災における取り組みと課題……竹下康平
コラム：いろんなチカラが集まったオンラインコミュニティ……松本雄一郎
コラム：震災復興のきっかけを紡いだクラウド……相羽大輔
コラム：そのとき，クラウドエンジニアはどう動いたか……後藤和貴
第3章：Amazon Elastic Beanstalkを使ってみよう……田中孝佳
第4章：AWS SDK for Android―手のひらから始まるクラウド体験……米林正明
第5章：RightScale―AWS対応クラウド運用管理プラットフォーム……荒井康宏，前佛雅人
```

さて本編。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/ihWeRUtp7x">pic.twitter.com/ihWeRUtp7x</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840457786228060160">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">罹災された方のほしい物リストの数。こんなにあると検索上位にある人しか買ってもらえない。 <a href="https://t.co/qkBH9QN6ri">pic.twitter.com/qkBH9QN6ri</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840461854094774272">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/uDZig2l2ph">pic.twitter.com/uDZig2l2ph</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840466027058151424">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/VSBSX4a6qP">pic.twitter.com/VSBSX4a6qP</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840473242854801409">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/CH8eC5aPJ7">pic.twitter.com/CH8eC5aPJ7</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/840473299834429440">2017年3月11日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

とにかく、回線さえきていればクラウドの力でいろいろなサポートができるぜということ。各社・各サービス結集で数日で罹災証明システムを作り出したという。すごい。

そうした行政支援という形が1つ。

そして「実際の災害発生現場において、行政の計画外の行動がでてしまった場合、誰がどのように支援するのか」という議題がとても興味深かった。[スマートサバイバープロジェクト](http://sspj.jp/)を参照すると理解が深まる。**「必要な人に　必要な支援を　必要な分だけ届ける」**

民間と地方自治体・国の関係はそもそも議論されるべきだが、結局「安全」をコミットするのは地方自治体・国なんじゃないだろうか？

民間（ツールによってとても便利に支援されたとしても）の助け合いに期待していますっていうのはなぜかボランティアが必要なときに集まるのが当たり前で、なんで集まらないんだろう？　そりゃ普通こねえよ！　という議論に近しい気もするんだが。現実はそうではないということなのだろうか？　そこも含めて深く議論したいものだ。


## 懇親会

うーん。疲れてた＆コミュ障のおかげでやっぱり盛り上がりについていけない系男子。会場外でまったりしてしまっていた。盛り上がっているのをそばできいている分には好き。


## 懇親会2nd （ソロ）

刀削麺、牛肉麺ぽい風味もして美味しかった。

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BRfqNiEBA2B/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">牛肉刀刀削麺</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)がシェアした投稿 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-03-11T10:35:15+00:00">2017 3月 11 2:35午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>


<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BRfqXPShKzE/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">麺が面白い&amp;美味しいなあ。</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)がシェアした投稿 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-03-11T10:36:35+00:00">2017 3月 11 2:36午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>


## 懇親会3rd

@aibaxさんに誘われて大懇親会場へ。みなさんお疲れ様でした！

久しぶりに英語勢に囲まれてやっぱ英語最低聞けるようにはなりたいなって思った…。いや開発してるならさ、問題とか課題とかコードとか設計にフォーカスしてるけどこういう何か話せとか言われてもコミュ障には無理です！　ごめんねえ。

記念撮影して終了！

## 懇親会4th

こういうでかいテーブル席のあるラーメン屋あってよかった。

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BRgIBKzhQ0S/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-03-11T14:55:42+00:00">2017 3月 11 6:55午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
