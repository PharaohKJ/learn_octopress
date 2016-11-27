---
layout: post
title: "Let's Encrypt での SSL 証明書を jenkins で自動更新するようにしたけれど"
date: 2016-11-27 12:31:17 +0900
comments: true
published: true
categories: 
---

こっちから `letsencrypt-auto renew` コマンドで更新するのってあちらから名前引いてインターネット側からこっちにつながらないとダメだよね?

弊社殆どのサービスは nginx でリバースプロキシし、「その名前でアクセスがあったらそのサービス(Docker / UNIX ドメインソケット / 別ホスト など)に割り振る」ようになっているので、「Let's Encrypt 側から認証アクセスがあったときだけはアプリモードじゃなくて認証モード」にせねばならぬ。

つまり、認証のその一瞬だけ nginx のリバースプロキシ設定外す必要あってアレだなーと躊躇し3か月に1度の25日あたりの更新時、毎度毎度手動でチャカチャカしてたのだが今日はクソ忙しいのにこんなことやらされて憤慨。結局 Jenkins にまかせることにした。

nginx 動いてるところに Jenkins に root で ssh 接続を許すのがイマイチ。やってることは 毎月25日になったら

``` shell-session
# ln -s -f /etc/nginx/conf.d/www.phalanxware.com.for_ssl /etc/nginx/conf.d/www.phalanxware.com.conf
# systemctl reload nginx
# /root/letsencrypt/letsencrypt-auto renew --force-renew
# ln -s -f /etc/nginx/conf.d/www.phalanxware.com.for_product /etc/nginx/conf.d/www.phalanxware.com.conf
# systemctl reload nginx
```

こんな感じで `ln -s -f` で nginx のリバースプロキシ設定を取り外して Let's Encrypt コマンドが認証時に置く認証用のファイルをちゃんと http GET できるようにする。更新が終わったらまた `ln -s -f` で元に戻す。ダウンタイムとしては1分はないかな?いまみたら上記実行に12秒かかったらしい。こういうログがちゃんと残るのが Jenkins のいいところだ。通知も slack に飛ばすようにしてるし、更新に失敗したらメールも飛ぶようになっている。

ここでは `www.phalanxware.com.conf` だけでやってるけれど、だるいだろうから `nginx.conf` あたりをかえてもいいだろうけれど、これすると全証明書更新終わるまでサービス再開できないのでダウンタイム伸びてしまうだろう。

しかしダウンタイムがあるのがダサいし、前述の通り Jenkins 側から root でつなげてしまうっていうのがどうしても気になる。まぁどうせ nginx サーバの接続ルールとして http / https 以外は Jenkins Server からしか ssh 接続許してないからこれでいいか。それがいやなら nginx サーバ自信で cron すりゃいいだけか。

