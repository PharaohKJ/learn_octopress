---
layout: post
title: "MultiConfig書いてみた"
date: 2015-09-19 15:56:53 +0900
comments: true
categories: Qiita Ruby
---

[Ruby - MultiConfigを書いてみた - Qiita](http://qiita.com/PharaohKJ/items/d166f0165aff99a3a996)

GitHubのREADME.mdを書いて、アレンジしてQiitaに書いて、さらにアレンジしてここに書くのは相当なアホらしさのでこんなところで。

`module EachConfig`が、最初は `class EachConfig < Hash` と作ってしまい、`EnvConfig`の実装にいたって「やってみるとclassがHashではない可能性大いにあるよなあ」となり、`class EachConfig` と `Hash` を多重継承したくなったが、これこそ `module` の出番であるとしてああなった。
