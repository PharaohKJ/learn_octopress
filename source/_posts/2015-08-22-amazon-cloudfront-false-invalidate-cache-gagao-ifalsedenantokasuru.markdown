---
layout: post
title: "Amazon CloudFront の invalidate cache が高いのでなんとかする"
date: 2015-08-22 06:58:23 +0900
comments: true
categories: aws
---

ちょっとみたら、 CloudFrontの料金が高くてビビる。(といっても$0.55)だが。

cdnのcacheをinvalidateし、更新するのにかかる料金が

  - 1,000 Path Requestまで無料

という条件を、1,000 Requestまでなんだろうなーと思ってたらどうやら本当に1URLにつき$0.005らしい。

こうなると、1回記事を書くとRSSだのカテゴリインデックスだのなんだのかんだので10ページは確実に
行き、結構お金かかっちゃうハメになってしまう。

だからといって、書いた記事が反映されるのが3日後とかになっても困るなぁーと思っていたら、

[AWS CloudFrontのinvalidationにワイルドカードが使えるようになりました。 ｜ Developers.IO](http://dev.classmethod.jp/cloud/aws/cloudfront-is-able-to-use-wildcard-on-invalidation/)

とあった。

まぁ1invalidate requestにURL含まれているし、俺関係無いわーと思っていたのに、関係あったらしいので、
これを採用しようと思う。

まず octopressの`s3cmd`を使っている部分を変更し、まったくinvalidateしないように。

```ruby
  # ok_failed system("s3cmd sync --no-mime-magic --cf-invalidate-default-index --acl-public --reduced-redundancy --cf-invalidate public/* s3://#{s3_bucket}/")
  ok_failed system("s3cmd sync --no-mime-magic --acl-public --reduced-redundancy public/* s3://#{s3_bucket}/")
```

つぎに、Dockerfileでrunコマンドを更新し、s3にdeploy後、awscliでinvalidate requestするようにした。

```Dockerfile
RUN pip install awscli
RUN aws configure set preview.cloudfront true
COPY _amazon.json /octopress.phalanxware.com/_amazon.json
CMD export PATH=/s3cmd-1.5.2:$PATH && export CRF=`date +"%Y%m%d%H%M%S"` && cd /octopress.phalanxware.com && git pull && cd /octopress.phalanxware.com && sed -i "s/__CRF__/$CRF/g" _amazon.json && rake gen_deploy && aws --profile octopress cloudfront create-invalidation --cli-input-json file://_amazon.json
```

とりあえずこの記事をpostしてテストしてみようと思う。

追記
----
`"CallerReference": "string"` ってのの理解が適当で悪かった。毎回違うものを発行しなければいけないらしい。（2重API呼び出し防止）
以下のページを参考にした。

[Amazon EC2 と Route 53 のはじめかた その 3 : Amazon Route 53 を試す - WebOS Goodies](http://webos-goodies.jp/archives/getting_started_with_amazon_ec2_and_route_53_volume_3_route_53.html)
[AWS CLIのパラメータをJSONファイルで記述する ｜ Developers.IO](http://dev.classmethod.jp/cloud/aws-cli-params-from-json/)

