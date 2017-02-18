---
layout: post
title: "『TDDBC Toyama #1』に参加した - DAY1"
date: 2017-02-19 01:11:57 +0900
comments: true
published: true
categories: event
---

テスト駆動開発ブートキャンプ（TDDBC）富山に参加した。

[TDDBC Toyama #1 - connpass](https://tddbc.connpass.com/event/47843/)

場所は[秀夢木楽館 ( しゅうむきらくかん )](http://www.yamahidehome.co.jp/kiraku/)でなんかすごい場所だった。airbnbなんかも提供しているらしい。

「テストコードはどうあるべきか？」というのがテスト原理主義の次のステージに進んでいて、とても学んだ。

特にテストコードを整理（DRY、MECEを目指す）できるのはテストコードを書いた人間のみというのがとても腑に落ちた。

「きたなくて動かないコード」が「キレイで動くコード」に変遷していくルートはどうあるべきかという議論はとてつもなくよかった。どこかでみなに問いかけたい。

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BQo7NwVBI-H/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">テスト駆動開発ブートキャンプはじまります！</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)がシェアした投稿 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-18T04:25:36+00:00">2017 2月 17 8:25午後 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">動かない＆汚い→動かない＆きれい→動く＆きれい。動かない＆汚い→動く＆きたない→動く＆きれい。この違いについて。<a href="https://twitter.com/hashtag/tddbct?src=hash">#tddbct</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832807413778505731">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="und" dir="ltr"><a href="https://t.co/v0A63RQHKP">pic.twitter.com/v0A63RQHKP</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832809192851283968">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">refactoring というラベルの呪い。やらなくてもいいという呪いか。</p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832809397088722944">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">TDDサイクルのコミットタイミングを考えると squash マージの要求がみえてくるな <a href="https://twitter.com/hashtag/tddbct?src=hash">#tddbct</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832809807283310594">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">テスト実行コストが落ちると、テストコードを書いてしまい、テストコードこそリファクタリングしないとそのメンテコストにやられる。1箇所変えたら1000箇所テストコードメンテする必要があるってなっちゃう。 <a href="https://twitter.com/hashtag/tddbct?src=hash">#tddbct</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832811806271758336">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">テストコードにこそ MECE DRY であるべき。 <a href="https://twitter.com/hashtag/tddbct?src=hash">#tddbct</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832811985381175300">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">コードの書き方に名前を付けているのはすばらしいな。</p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832820391735222272">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">テストコードを最小限に抑えるのはテストコードかくひとの役目。 <a href="https://twitter.com/hashtag/tddbct?src=hash">#tddbct</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832825296055214080">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">Rubyがメジャーなのは確定的に明らか <a href="https://t.co/domguJWUpr">pic.twitter.com/domguJWUpr</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/832895943087267840">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## 懇親会

ピザとオードブルだったが…。@nagise先生がご登場いただいて以下を振る舞われた。ありがとうございます！

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">本日のメニュー<br>-ブリしゃぶ<br>-ブリかま焼き<br>-フグしゃぶ<br>-カワハギ(肝付き<br>-イワシの刺身<br>-ホタルイカ(ゆで)(しゃぶしゃぶ)<br><br>まだ出してないのが幾つか……</p>&mdash; なぎせ ゆうき (@nagise) <a href="https://twitter.com/nagise/status/832917916970528768">2017年2月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BQpjVWGhIps/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-18T10:16:10+00:00">2017 2月 18 2:16午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>


## 風呂

[となみのゆ（富山県砺波市）－日帰り温泉の検索：デイ温泉ドットコム](http://www.day-onsen.com/sisetu/2/sisetu2596_home.html)にお邪魔した。ジャパニーズトラディショナル銭湯に近く、趣深くてよかった。もちろんシメにコーヒー牛乳を飲んだ。

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BQqAACbBHT6/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">風呂上がりにはこれでしょ！！ #tddbct</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">cotton_desuさん(@cotton_desu)がシェアした投稿 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-18T14:26:40+00:00">2017 2月 18 6:26午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

