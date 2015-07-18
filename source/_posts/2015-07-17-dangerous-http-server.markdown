---
layout: post
title: "dangerous http server"
date: 2015-07-17 12:10:23 +0900
comments: true
categories: docker
---

どうやらそろそろ 1.0 になりそうな Google Kubernetes を触ったりしているのだが、
([Announcing Kubernetes 1.0 July 21, 2015 | Oregon Convention Center](http://www.kuberneteslaunch.com)だとさ)
こういった、docker container 前提の cluster 上に えいや とお願いすると、cluster
上の **どこか** の computer (VM instance) に配置され、動き始めるという作りに
なっている。

これがまた、結果として

- どこの computer で
- どんな 環境変数など で
- ちゃんと 他のcontainer にアクセスできるか
- 調査コマンドを送りたい・・・

というようなことを調べる/やるのがだいたい厄介で(そもそも気にしなくていいように
作っているのが利点なのですし)、だからこそ fluentd とかが必須となってくる
のだろうけれど、調査のためにいろいろ用意しなくても、そのcontainer配置機能を
活かして簡単にできないかな？ということで危険なhttp server を作成しました。

[pharaohkj/sheller](https://registry.hub.docker.com/u/pharaohkj/sheller/)

Information に書いてある通り、 port 9292 で動作するhttp server で、`curl -d 'cmd=whoami' http://deploy_ip:9292/shell`とかすると、`cmd=`の内容を ruby の`system`を
行ってその内容を返すという、セキュリティのセも無い container である。`.env`を
http get すれば hostname とかも得られるのでぜひお試しあれ。

とくに`docker --link`とか`kubectl create -f service.yaml`とかして、環境変数が
超大事な人とかにはマジオススメ。
