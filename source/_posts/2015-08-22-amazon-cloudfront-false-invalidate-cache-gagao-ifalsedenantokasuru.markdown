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

```Rakfile
  # ok_failed system("s3cmd sync --no-mime-magic --cf-invalidate-default-index --acl-public --reduced-redundancy --cf-invalidate public/* s3://#{s3_bucket}/")
  ok_failed system("s3cmd sync --no-mime-magic --acl-public --reduced-redundancy public/* s3://#{s3_bucket}/")
```

つぎに、Dockerfileでrunコマンドを更新し、s3にdeploy後、awscliでinvalidate requestするようにした。

```Dockerfile
RUN pip install awscli
CMD export PATH=/s3cmd-1.5.2:$PATH && cd /octopress.phalanxware.com && git pull && cd /octopress.phalanxware.com && rake gen_deploy && aws --profile octopress cloudfront create-invalidation --distribution-id $DIST_ID  --invalidation-batch '{"Paths": { "Quantity": 1, "Items": ["/*"] }, "CallerReference": "string" }'
```

とりあえずこの記事をpostしてテストしてみようと思う。
