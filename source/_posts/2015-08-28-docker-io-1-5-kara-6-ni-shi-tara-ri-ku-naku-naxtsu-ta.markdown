---
layout: post
title: "docker-io 1.5 から docker-io 1.6 にしたらリークしなくなった"
date: 2015-08-28 16:50:52 +0900
comments: true
categories: docker
---

さくらのVPSにおいて、CentOS6上でDockerを運用している。そのDockerが1.5系から1.6系にUpgradeされた結果、メモリリークがなくなった。

以下はmuninのスクショである。ちなみに、定期的に下がっているのは6時間毎に `/etc/init.d/docker restart` しているからである。

{% img https://dl.dropboxusercontent.com/s/gf8tyf7j13wvbvo/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88%202015-08-30%2018.03.01.png munin %}

これでちょっと安心できる。
