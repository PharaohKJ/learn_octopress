---
layout: post
title: "節約できてない"
date: 2015-07-28 11:24:23 +0900
comments: true
categories: さくらVPS, AWS
---

1日、アクセスログの容量だけ持てばいいapache(m3.medium) + RDSじゃないEC2のDBで結構な容量(m3.medium)

という構成で運用しているサービスがあるのだが、さくらVPS(石狩:HDD200G)上で動いているjenkinsで定期バックアップを毎深夜取るという運用にしている。

なんだかんだでEBSやs3の料金もバカにならないからねー。さくらVPSと併用で節約！と思ってたら、DBが大きくなってきて、AWSから外にでるdata transfer料金が取られるようになってきた・・・。

ちなみにお値段は

> $0.140 per GB - up to 10 TB / month data transfer out

である。DBはmysqldumpでbackupしているんだが、毎日1G だと

**`30日 x $0.140 x ￥125/$ = ￥525`**

結構いっちゃうんだなあ。いや、さくらVPSが￥1500/月なわけで、予算が数百円単位だとどうしてもでかくなっちゃう。

gzipしているので、AWS側でgzipすればだいぶ節約できるかもしれない。
