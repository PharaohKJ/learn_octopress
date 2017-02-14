---
layout: post
title: "『JAWS-UG金沢 第19回 平日勉強会』に参加しMQTTについて少し話した"
date: 2017-02-15 08:25:42 +0900
comments: true
published: true
categories: JAWS-UG 
---

今回はIoTについて。

最近はいろいろなインフラが整ってていて嬉しいなんでもHTTPですませよう！　的な動きがあるが、やはり「餅は餅屋」である。その餅屋、すなわち、MQTTを使おう！　という話をした。

[JAWS-UG金沢 第19回 平日勉強会](https://jaws-ug.jp/es/kanazawa19/)

そしてちょっと間に合わなかったがAWSのCLIを使って

- MQTTブローカのサーバをたてずに（= EC2レス）
- デバイスを登録してクライアント証明を作成し
- それをつかってsubscribe待機
- それをつかってpublish

という流れを見せた。

時間がない、と言い訳したがちょっとこれは真面目にMQTTの資料は今後必要になってくるのでがんばって作ろうと思う。結局、たくさんのデバイスから効率よく情報を集めたり、それらを相互に通信するための専用プロトコルがあり、それを使うほうが断然有利だという資料を作っておきたい。


## 「IoTからの – AWS」Tから初めてI（AWS）にたどり着くまで 宮川さん

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:40.23148148148148% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BQVa_C3AJz7/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-10T14:38:24+00:00">2017 2月 10 6:38午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

ISDNで構築していたインフラ網を無線（SORACOM）とAWS（IoT）に置き換えていくぜという話。

質疑では「普通の会社では、クラウドの採用というだけで拒否反応されてしまう。宮川さんはどうして採用できたのか？」という問がでたが、これはまとめると「宮川さんにある程度決定権がある」ということが大体だたようだ。

やはり決定権のある人（CIOとかCTOとかほとんどの場合は経営者）が、ライバルがどうやってるか常に考えている会社は強そうだ。

決定権のある人がJAWS-UG金沢にきていただているという、とても希望ある話でよかった。


## HomeKit（siriで家電を操作） 香川さん

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:37.5% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BQVbBGYgfaI/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-10T14:38:41+00:00">2017 2月 10 6:38午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

<blockquote class="instagram-media" data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:45.78703703703704% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/p/BQVbCpjASXF/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">ふぁらお加藤さん(@pharaohkj)がシェアした投稿</a> - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2017-02-10T14:38:54+00:00">2017 2月 10 6:38午前 PST</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

[nfarina/homebridge: HomeKit support for the impatient](https://github.com/nfarina/homebridge)

HomeKitデバイスのふりをしてくれるソフトウェアがあり、それ経由で

- 扇風機を回したり
- ライトをつけたり
- 「おやすみ」というと同時に消えたり
- 「おはよう」というと同時についたり

というデモンストレーションを見せていただいた。これは素晴らしい！

普通、こういうのは早々と対策されてしまうのだがこれは結構お目こぼしされているとのこと。

　日本でHomeKit対応製品なんてほとんどないだろうしこういうの経由でいろいろと使い初めることで、やっと「こうあるべき」「あああるべき」と議論できるだろうので、もっと普及してもらいたいものだ。


## 懇親会

[土火楽 | 武蔵商店街振興組合公式ウェブサイト](http://kanazawa-musashi.com/shop/dokaraku.html)

当日参加者全員の7人で土火楽に行った。いやーあいかわらずここのモツ鍋おいしいわー。オススメ。


