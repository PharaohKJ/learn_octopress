---
layout: post
title: "やっぱりmapファイルができてしまう件と犯人は違ってた？"
date: 2017-11-16 12:53:00 +0900
comments: true
published: true
categories: life
---

やっぱりサイト再作成が遅い！コイツはめちゃ許せん！ていうか毎回やっぱりマップファイルできちゃってるじゃん！

とわかっていろいろやって、やっぱJekyllのバージョンあげないとダメかなあと思ってたが、静的サイトジェネレータのコードを読むのも悪くないと思ってちょろっと読んだ。最初のモチベーションは「出力OFF設定してるのにそのパラメータがなぜ伝わらないのか」を確認するつもりであった。

とりあえずいろいろなジェネレータを使ってサイト作成しているのは `gems/jekyll-2.5.3/lib/jekyll/site.rb` の以下だ。Jekyllのバージョンが古いのは勘弁してくれ。

```ruby
    # Run each of the Generators.
    #
    # Returns nothing.
    def generate
      generators.each do |generator|
        generator.generate(self)
      end
    end
```

んー抽象度高いので、generatorインスタンスの正体から炙り出そうと思ってこのループに `p generator` 加えてみたら、あきらかに遅いヤツがいる。ははーコイツだなあ。一番遅いヤツを炙り出すためちょっと詳しくログ出してみる。

```ruby
    # Run each of the Generators.
    #
    # Returns nothing.
    def generate
      generators.each do |generator|
        before = Time.now
        Jekyll.logger.error ['Generate Start', generator.to_s, Time.now]
        generator.generate(self)
        after = Time.now
        Jekyll.logger.error ['Generate End', generator.to_s, Time.now, after-before]
      end
    end
```

結果

```
["Generate Start", "#<Jekyll::GenerateCategories:0x007f7fcf837ce0>", 2017-11-16 13:35:09 +0900]
["Generate End", "#<Jekyll::GenerateCategories:0x007f7fcf837ce0>", 2017-11-16 13:35:14 +0900, 4.982982]
["Generate Start", "#<Jekyll::JekyllSitemap:0x007f7fcf837cb8>", 2017-11-16 13:35:14 +0900]
["Generate End", "#<Jekyll::JekyllSitemap:0x007f7fcf837cb8>", 2017-11-16 13:35:14 +0900, 0.054229]
["Generate Start", "#<Jekyll::Paginate::Pagination:0x007f7fcf837b28>", 2017-11-16 13:35:14 +0900]
["Generate End", "#<Jekyll::Paginate::Pagination:0x007f7fcf837b28>", 2017-11-16 13:35:14 +0900, 0.010508]
```

んんん〜カテゴリ一覧作成が5秒ぐらいかかっとるやん？　試しにカテゴリを削ってみると

```ruby
["Generate Start", "#<Jekyll::GenerateCategories:0x007f7fcf837ce0>", 2017-11-16 13:38:14 +0900]
["Generate End", "#<Jekyll::GenerateCategories:0x007f7fcf837ce0>", 2017-11-16 13:38:15 +0900, 0.019338]
["Generate Start", "#<Jekyll::JekyllSitemap:0x007f7fcf837cb8>", 2017-11-16 13:38:15 +0900]
["Generate End", "#<Jekyll::JekyllSitemap:0x007f7fcf837cb8>", 2017-11-16 13:38:15 +0900, 0.009151]
["Generate Start", "#<Jekyll::Paginate::Pagination:0x007f7fcf837b28>", 2017-11-16 13:38:15 +0900]
["Generate End", "#<Jekyll::Paginate::Pagination:0x007f7fcf837b28>", 2017-11-16 13:38:15 +0900, 0.001491]
```

0.02秒！　これは俺の求めてた速度だわ。今カテゴリはデフォルトで全カテゴリが設定されるように改造済み、そうじゃないものを消すような運用にしていたんだよね。俺が。つまり犯人は俺。
