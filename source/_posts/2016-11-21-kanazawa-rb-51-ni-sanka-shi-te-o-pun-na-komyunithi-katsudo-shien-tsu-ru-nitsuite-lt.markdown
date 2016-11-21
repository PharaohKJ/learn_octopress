---
layout: post
title: "『Kanazawa.rb #51』に参加してオープンなコミュニティ活動支援ツールについてLT"
date: 2016-11-21 21:30:17 +0900
comments: true
published: true
categories: 
---

[kanazawa.rb meetup #51](https://kzrb.doorkeeper.jp/events/53553) に参加して LT した。

<iframe src="//www.slideshare.net/slideshow/embed_code/key/dkng2EoPGRam9E" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/pharaohkj/ss-69290663" title="俺とコミュニティ活動のタスク" target="_blank">俺とコミュニティ活動のタスク</a> </strong> from <strong><a target="_blank" href="//www.slideshare.net/pharaohkj">Masayuki KaToH</a></strong> </div>

最近、 doorkeeper さんが無料プランの廃止を打ち出して結構熱い感じのこの界隈だが、どのツールも「開催者が複数で、分業し、裏方の決めておいたほうがいいノウハウをシェアする」という部分が弱い気がするんだよね。ビッグビジネスになる気もする…。いやなってたら doorkeeper さんがあんなことにならんか。ははは。

あと、当日やろうとしていた tDiary の静的サイト化は、

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/tdtds">@tdtds</a> <a href="https://twitter.com/PharaohKJ">@PharaohKJ</a> 今でも使っていて最新のコードは <a href="https://t.co/tF9M1dKyxX">https://t.co/tF9M1dKyxX</a> にありますが、ツッコミができないので普通のtDiaryユーザーにはおすすめしません。。。</p>&mdash; す (@ktou) <a href="https://twitter.com/ktou/status/777648582362935296">2016年9月18日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

で教えていただいた内容でやってみようとがんばったが…。Gem でインストールする tDiary はすでに `core/tdiay.rb` がないんじゃないか?ってところで詰まって試せずやめてしまった。 docker 運用だってのもあって、めんどい度が高かった。

今(2016-11-21 22時現在)、ちょろっと読んでみたら、特に `core/tdiary.rb` がいらなくて、 `lib` のディレクトリさえわかればいいんじゃないか?って読めた。

懇親会はモツ鍋うさぎ。いつもいきすぎて写真がない! 酒飲んでないのに何しゃべったかとっても記憶がないんだけれど、ソフト屋じゃない子にいろいろ説教した気がする。確か「俺、営業の人にだまっても売れるもの作れ」って言われたので「石油でも売ればいいのに」というネタがあるんだけど、リアルに石油売ってる人と話しちゃったよ。ぐらいのネタがあったような…。


