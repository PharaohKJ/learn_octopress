---
layout: post
title: "Ruby GEM 『pomo』 を使い始めた"
date: 2016-05-06 23:57:57 +0900
comments: true
published: true
categories: ポモドーロ・テクニック
---

本家本元は数年とまっているようなので、fork先の [attomos/pomo: Ruby Pomodoro app for the command-line (time / task management)](https://github.com/attomos/pomo) を使わせていただいた。

``` shell-session
$ git clone https://github.com/attomos/pomo.git
$ cd pomo
$ bundle install && bundle exec rake build && gem install pkg/*.gem
$ pomo initconfig --notifier notification_center
```

`init` するとき、`notification_center` を指定しないと、 growl が採用されてしまうので注意。ここまでできたらあとは

``` shell-session
pomo add "ユーザーレコード編集画面を作る"
```

でタスクを追加し

``` shell-session
pomo start
```

とすれば、Kyokoさんの声で開始した旨読み上げられ、半分経過、残り5分、フィニッシュまで読み上げられる。しかし、日本語の音声だと読み上げがヒドイ。

そして `list` などで、これまでの結果なども取ることができるようだ。シンプルに `~/.pomo` にタスクが保存されている。これを Dropbox などで share すれば、どこのコンピュータいっても持って回れそうだし、デイリーレポートを作ったり、振り返りしたいときもこれでなんとかなりそう。

ちょっと、使い込んでいこうと思います。
