---
layout: post
title: "このページについて"
date: 2015-07-17 11:18:35 +0900
comments: true
categories: 
---

[About](/about/) を書いてみたのだが、自動的にはトップページからリンクが張られないのだなあ。

```console
[pharaohkj]$ be rake -T
rake new_page[filename]        # Create a new page in source/(filename)/index.markdown
```

としたら、[filename]とあるが、これはどうやって指定するのだ？と思ったらまさかの

```console
[pharaohkj]$ be rake new_page[about]
```

と書くという・・・。こういう指定とは一般的なのか？たくさん Rakefile 書いてきたつもりだったが他人のものを見るのが足りなかったか。中身を読んだがparseはrakeがやってくれてるのかな？今後は導入してみよう。
