---
layout: post
title: "『TDDBC Toyama #1』に参加した - DAY2"
date: 2017-02-25 12:30:34 +0900
comments: true
published: true
categories: 勉強会
---

## カードゲーム

3時頃、みんなテンアゲだったし、せっかく持ってきたのでカードゲームに興じる。

選んだタイトルは[チルノのさんすうゲーム](http://www.gamers-jp.com/playgame/db_gamea.php?game_id=4905)。

朝4時ごろまでがんばった気がする。


## 『実践テスト駆動開発』を読み込む

朝4時ごろ、寝静まった。このチャンスを生かして講師の[Takuto Wada(@t_wada)さん](https://twitter.com/t_wada)がお持ちになった本を読破することに挑戦することにした。

朝までは3時間程度しかないので、しょうがなく以下の本をチョイス。

<a href="https://www.amazon.co.jp/%E3%83%86%E3%82%B9%E3%83%88%E9%A7%86%E5%8B%95%E9%96%8B%E7%99%BA%E5%85%A5%E9%96%80-%E3%82%B1%E3%83%B3%E3%83%88-%E3%83%99%E3%83%83%E3%82%AF/dp/4894717115/ref=as_li_ss_il?ie=UTF8&qid=1487998479&sr=8-1&keywords=%E3%83%86%E3%82%B9%E3%83%88%E9%A7%86%E5%8B%95%E9%96%8B%E7%99%BA%E5%85%A5%E9%96%80&linkCode=li3&tag=pharaohkj-22&linkId=537db971cd236073321cbb8a4a947ec0" target="_blank"><img border="0" src="//ws-fe.amazon-adsystem.com/widgets/q?_encoding=UTF8&ASIN=4894717115&Format=_SL250_&ID=AsinImage&MarketPlace=JP&ServiceVersion=20070822&WS=1&tag=pharaohkj-22" ></a><img src="https://ir-jp.amazon-adsystem.com/e/ir?t=pharaohkj-22&l=li3&o=9&a=4894717115" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />


<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">テスト駆動開発入門読んだがこれはすごいな。こんなこと真面目に書くのがすごい。ライブ感がぱない。</p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/833076826536751104">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

機能を足した動くコード→よりよいコードをガンガン書いていくライブ感がすごい！

私とかが「慣れろ」で済ませることをちゃんとまとめてあってすごい。プログラム書けるようにはなったけどプロってどんなふうに進めているんだろう？　ぐらいの学生や、少し書き始めてきた人間にとてもオススメしたい。

90分ほど寝る。


## 朝食

健康によさそうな内容だったので完全にブッチして昨日の残りのピザなんかを食べた。


## クソコード鑑賞会

まぁクソコードであるが、このコードを書いた人の実力がこれなのか、それともここからまだリファクタできると思ってるのかはわからない。

### 捨てる勇気

正しいバージョン管理ソフトを使って大量のコメントアウトを捨てよ。正しくバージョン管理システムが動いているところにおいては、コメントすら「必要なのである」としてメンテナンス対象となるのでツライ。

DAY1で習ったとおり、捨てられるのは真意がわかっている人すなわち書いた本人のみである。がんばりたい。

### チケットベース開発はいいがやはりコードメンテナとレビューがなければこうなる

対象のコードはビューも含めたウェブアプリのコードだったんだが「内部構造はよくわからないが内部を把握する時間や予算がなかったので、がんばって機能を増やした」というあがきを感じる。

こうなるのはまともなメンテナ（もしくはレビュア）が用意できないなかでチケットベースで指示やバグフィックスをがんばってやるとどうしてもこうなる。

何を申したいかというと、クソコードになるのはクソコードを書いた人間だけをあれこれ言っても解決できず、「仕事のやりかた」「予算のかけかた」などのスコープからも見ないとそりゃクソコードになるわい。ということが言いたい。



## レガシーリファクタリング

ライフゲームとお伺いしていたのだが、まさかの「もう動いているライフゲーム」に

- リファクタリングと
- テストを加えよ

というかなり実践的な内容。

いろいろあって、Rubyチームを離れてJavaチームに入った。そのおかげでIntelliJを触る機会を得られて大変よかった。

強力な変数・関数のリネーム機能もあったりしてJavaの強みを活かしていろんなことできてよかった。

とか言いながら、2次元配列を扱うのにXとYを間違えてリネームしてしまったばっかりにハマってしまった。Xを指定してその座標の集合がとれるというテストをまともにやるべきだったか。慢心だな。


## お昼ごはん

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BQrZ3EShPk3/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-19T03:31:52+00:00">2017 2月 18 7:31午後 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>


## KPT

前述したが今回の内容では

「プログラム書けるようにはなったけどプロってどんなふうに進めているんだろう？　ぐらいの学生や、少し書き始めてきた人間にとてもオススメしたい」

次はこういうものをいかに会社に持ち込むか。どのようなツールが支援してくれるのか。をノウハウとして持ち寄って議論したい。…いや俺無職だった！

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BQruNLEhGjY/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-19T06:29:39+00:00">2017 2月 18 10:29午後 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## 解散

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">終了！おつかれさまでした！<a href="https://twitter.com/hashtag/tddbct?src=hash">#tddbct</a> <a href="https://t.co/5JlHrC493F">pic.twitter.com/5JlHrC493F</a></p>&mdash; mugi (@mugi_uno) <a href="https://twitter.com/mugi_uno/status/833215510238023680">2017年2月19日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
