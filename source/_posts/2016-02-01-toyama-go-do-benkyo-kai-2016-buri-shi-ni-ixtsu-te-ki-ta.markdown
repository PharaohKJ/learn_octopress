---
layout: post
title: "『富山合同勉強会2016 ～ぶりしゃぶ会～』に行ってきた & 松江のワークショップを宣伝してきた"
date: 2016-02-01 11:35:11 +0900
comments: true
categories: 勉強会
---

2016/1/30(土) に行われました

[富山合同勉強会2016 - connpass](http://toyama-eng.connpass.com/event/24840/)
[富山合同勉強会2016 【懇親会用】 - connpass](http://toyama-eng.connpass.com/event/24866/)

に参加してきました。ついでに、松江のワークショップもちょっと宣伝してきました。会場は「.NET枠」と「Java枠」で、場違い感がありますが、完全に学ばせていただこうと思いました。

# 基調講演 - 日本マイクロソフト株式会社　エバンジェリスト井上 章さん 『ぶりと .NET と Visual Studio ～ その構想及び傾向と対策に関する一考察』

井上 章さんとはいろいろ縁が深いこともありますが、やっぱり .NET の動向は気になります。パッケージマネージャの話で、MS社製ではなく、サードパーティのものを積極的に使ってる & インテグレーションもしている、というデモを確認。

やはり、 Visual Studio Code はスゴイ。でもなんていうのかなぁ。MSのやるならWindowsでVisual Studio使うぜ！という私の考えは変わらないので、なかなか使う機会が無いかもしれない。ガチで使ってみないとなあ。ただまあ、フロントエンド周りはとっても疎いので、どこからやらないといけないのかピンとこない。

それらに代表される、Microsoftの方針がいろいろきけてよかった。


# 桜庭さん 『Project Jigsawではじめるモジュール』

モジュールとは何か。

[モジュール - Wikipedia](https://ja.wikipedia.org/wiki/%E3%83%A2%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB#.E3.82.BD.E3.83.95.E3.83.88.E3.82.A6.E3.82.A7.E3.82.A2)

まぁーこのように定義されているが、実際の議論における「モジュール」って割とフリーダムである。

今回のここでいう「モジュール」は、DLLとかGEM、jarの話である。

ユーザーがモジュールから得られる機能 == モジュール実装者が公開したい機能、と、実装における「public」が一致しないため、苦労するという話。その問題を「過去のものと互換を保ちつつ、実装した」という話。うーん素晴らしい。

シンプルに、定義ファイルで定義し、そのファイルがなければ旧動作、定義ファイルを書くサポートツールも提供する、という感じだったが、public な public など、地獄を渡ったのがかいま見える・・・。


# 寺田さん 『Microsoft Java』

こちらも井上さんと同じく、MSは他を叩き潰すのではなく、共同していく、という話。しかもそれが元Oracleの方からレポートしていただけるというのはとても貴重であった。Azureの受けている誤解などなど、いろいろな現場の話をきけてマジでよかった。


# @kunitooさん 『Ruby 2.3 のてざわり』 @flada_auxvさん 『わたしの Ruby の楽しみ方』

ガチRubyistじゃないとピンとこないんじゃないかなぁーと思ったが、いろいろツッコミが入ってよかったな。桜庭さんのように「抱えていた問題と解決法」という流れで話したほうが通じたかもなと思った。


# 情報支援レスキュー隊(IT DART)　酒井 佑弥さん 『エンジニアが出来る貢献』

災害系は私が最初にやったシステムだし、CfK的な動きはやっぱり全国的なんだなあと。そしてこういう「予算が無いのをどうクリアしたか」というのはすっごい後ろ向きすぎてイヤなんだが、向き合わないといけない「現実」であり、話をきけてとてもよかった。

ただまあ、こういうところ = 日本国が災害のときに使おう、予算が無いときに使おう、というのにででてくるインフラに「まっっったく日本のSaaSやPaaSがでてこない」というのがすごい残念に思う。まぁここらで使ってるデータセンターを構成する部品や重工業的なところで日本がでてくるのかもしれないが・・・。結局そういうところの顔が見えないというのはとてつもなくもったいないだろう。


# LT枠

無理やり3分だけねじ込んでもらって

[DataCenter とソフトウェア開発ワークショップ](http://dcworkshop.github.io/201602/0_about.html)

の宣伝してきました。秀和さんのRubyエンジニアさんもいらっしゃったので響くといいな・・・。


# 懇親会

割烹 扇さんでぶりしゃぶを含むコース。

9,000円 + お酒代というお高い会費を払っただけはあるうまさ！「ぶりしゃぶ」なんて日本酒炎の酒鍋、孤独のグルメゴローちゃんだけの話だと思ってたら自分が体験できました！！感動する美味しさ。また行きたいズラ・・・。ていうか自宅でもできるんじゃないか？いやいや日本酒一升瓶をまるまる鍋にするなんて・・・。ああ贅沢！！！

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="6" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BBKQjvtkz6n/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">ぶり絨毯！！！</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した写真 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-01-30T10:44:44+00:00">2016 1月 30 2:44午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="6" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BBNI9W-Ez9Q/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">昨日の写真の続き。お刺身。</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した写真 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-01-31T13:36:03+00:00">2016 1月 31 5:36午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="6" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BBNJRDfkz95/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">お昼のスーパーマーケットのフードコートとお好み焼きおいしかった。こういうの焼けるようになりたい。</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した写真 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-01-31T13:38:44+00:00">2016 1月 31 5:38午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
