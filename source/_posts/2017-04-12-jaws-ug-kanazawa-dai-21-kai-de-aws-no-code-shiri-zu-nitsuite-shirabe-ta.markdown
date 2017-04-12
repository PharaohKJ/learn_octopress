---
layout: post
title: "『JAWS-UG金沢 第21回』でAWSのCodeシリーズについて調べた"
date: 2017-04-12 09:27:01 +0900
comments: true
published: true
categories: AWS JAWS-UG
---

[JAWS-UG金沢 第21回 週末勉強会 もくもく & 質問大会 - JAWS-UG 金沢 | Doorkeeper](https://jawsug-kanazawa.doorkeeper.jp/events/58885) に参加した。あやうくソロでもくもく & 自問自答会になるところであったがなんとか3人で実施。質問はなかった。

## 無料でプライベートリポジトリ CodeCommit

[Amazon CodeCommit（安全でスケーラブルなマネージド型ソースコントロールサービス） | AWS](https://aws.amazon.com/jp/codecommit/)

そもそもリポジトリがプライベートなのは当たり前のはずなんだが現実そうでもない。みなで協業、デプロイ先からpullするにしても、パブリッククラウド上にVCS系を導入するのが一番現実的である。

と、そうなると認証系がどうしてもめんどくなる。そのあたりをIAMで処理できるし、他社サービスやAWSサービスとの連携が容易なのがいいところ。

あと無料枠がでかいので実質無料だ。GitHubと違って1ファイルあたりのサイズ制限は実質ない。5人以上のプロジェクトなんざしらん。 → [料金 - Amazon CodeCommit | AWS](https://aws.amazon.com/jp/codecommit/pricing/)

ユーザーを認証情報を追加するの一番楽なのはたぶん以下の手順。そもそもSSH鍵の扱いに慣れていればSSHを使うのが一番楽そう。

IAM > サイドバーからユーザー > ユーザーを選択（なければ作成） > 概要画面から認証情報タブをクリック > 最下段の **AWS CodeCommit の HTTPS Git 認証情報** の生成ボタン

日本リージョンに現時点で無いってのが残念だけど！


## CIサービス CodeBuild

[AWS CodeBuild (完全マネージド型ビルドサービス) | AWS](https://aws.amazon.com/jp/codebuild/)

GitHubからCircleCIやTravis CIを活用している人ならピンとくる、それに相当するサービス。

1. ソースコードをどこからか持ってきて
2. ビルド処理を使い捨てVMインスタンスでビルドし
3. 結果や成果物をS3に置ける

ということに特化している。 1.についてはCodeCommitやGitHub、S3からzipをとってくるってのが選べたり、2.についてはどんな環境であれこれするってのを `buildspec.yml` というファイルで指示できたりVMの仕様を決めたりできるというもの。

料金はこのビルド時のみ自動で起動・終了するVMインスタンス分だけ支払えばよいようだ。そして最初の100分は無料。特に何もインストールしないで Ruby 2.3 のVM選んで `puts 'hello world'` するだけでも5分ぐらい使った。真面目に運用始めたら無料には収まらなさそうだな。


## デプロイエージェント CodeDeploy

[AWS CodeDeploy (EC2 インスタンスへのコードデプロイを自動化） | AWS](https://aws.amazon.com/jp/codedeploy/)

AWS上のVMサーバ、つまりEC2上に都合よくデプロイするエージェント。他社PaaSにデプロイしたりするわけじゃない。それだけ把握すれば今回はじゅうぶん。なかなか低予算でたくさんのEC2インスタンスにちゃんとデプロイするって要求はなかなかないのが現実。


## Codeシリーズのオーケストレーション CodePipeline

上記3つをオーケストレーションする。ウェブコンソールにはいってマウスでポチポチ決められるのはおもしろい。

1パイプラインだけは無料。以降、1パイプライン/ドル。


## 統括

AWS内で全部完結するならば、AWS上にJenkinsインスタンスを持つよりこっちでいろいろ処理したほうが管理すべきものが減るのかもしれない。やることを絞れば覚える手数が減って手軽に導入できるかな？

まーいま『Jenkins職人問題』がでちゃうほど、Jenkinsがなんでもできるうえに設定が煩雑、覚えること多いってなってるので、AWS CLIでちゃんと操作できてこの設定をコード化できればバッチリだろうなあ。


## 懇親会

加能商店さんにまた突撃した。今日のMVPはスパイシースペアリブだ。ローストオニオンとスパイスたっぷりで肉もよく焼けててめちゃうまかった。

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:49.76851851851852% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BSutkGDBe70/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-04-11T03:24:33+00:00">2017 4月 10 8:24午後 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>


<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BSutuoJBMSy/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-04-11T03:25:59+00:00">2017 4月 10 8:25午後 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
