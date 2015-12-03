---
layout: post
title: "VR Game Jam 石川会場にて参加"
date: 2015-12-04 00:45:19 +0900
comments: true
categories: VR, GameJam, Hackathon
---

[第4回 Oculus Game Jam in Japan 石川会場 - 金沢ゲーム制作者コミュニティ | Doorkeeper](https://kzgame.doorkeeper.jp/events/33759) に参加した。

メンツは勝手知ったる少人数のメンツゆえ、気楽に参加できましたが、勝手知ったるとは言え、VR(=Oculus)なれしてるかどうかなど考えて1チームで1本作ることにした。

# できたもの

今回はbitbucket上にヒミツリポジトリとして作成した。

- コンセプトはユニティちゃん鬼ごっこ
- 各プレイヤーは箱庭のなかにランダムなポジションで登場し、それぞれおいかける
- パックマン方式で、でたアイテムを取得した側が一定時間鬼

やはりVRはスゴイ、GBの対戦のときのスゴイ版であり、やはり対戦ゲームは全員別々の視点のゲームとそうじゃないのでは  
世界が違うな！

# スポンサースゴイ

## RedBull飲み放題

まさかのシュガーレスあり。そしてまさかの冷蔵庫を貸していただけるというスゴさ。みんな写真とってSNSにもあげるし、効果は抜群だ！

## Photonがスゴイ

[世界最大級のオンラインゲーム開発エンジン｜Photon Realtime 日本スペシャルサイト](http://photoncloud.jp/)がスゴイし川滝さんもスゴくて
あっというまにUnityで対戦ゲームの基盤ができちゃった。無料枠もあるようだし、これは抑えておかねばなるまい。


# 反省点

## もっと少人数にすべきだった

いわゆる「プログラマ」という人間5人で全員でやるというのはよくなかった。やはり「みんな暇にならないように」
と考えてしまった。その「暇」というのも大いなる勘違いなのだが・・・。


## 機能を増やしてしまった

スプリントの区切りで「次何しようか？」となったとき、機能を増やしてしまったのは失敗だった。

- マージに時間がかかる
- 仕様の共有に時間がかかる

のは見えていたのに。次はもっと「ゲームぽい演出」の作りこみに時間をかけるべきであったろう。


## 俺はstaticおじさん

ゲーム開始・ゲーム中・ゲーム終了スコア表示的なシーン跨ぎのデータを作成する際、破棄されないclassを  
作ったはいいが、いつインスタンス化されるかピンとこなかったので、全部staticで作ってしまった・・・。


## 動きの少ないゲーム

疾走感あふれるのがVRゲームとしてはステキなんじゃないか！？と思ったんだが3D酔いを初体験。  
いままで3Dゲームで酔ったことなんてなかったが、鬼ごっこゲームで周りを見ながら走ったりしたら、  
ベロベロになって30分ぐらいマジで寝込んだ。作るならまったりスニークアクションとかのがいいだろう・・・。

# 写真

みんなありがとうございました！

<blockquote class="instagram-media" data-instgrm-version="6" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/-1vehzkz8s/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)が投稿した写真</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2015-12-03T18:28:04+00:00">2015 12月 3 10:28午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
