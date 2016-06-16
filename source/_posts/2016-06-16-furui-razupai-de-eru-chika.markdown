---
layout: post
title: "古いラズパイでエルーチカ"
date: 2016-06-16 00:37:25 +0900
comments: true
published: true
categories: IoT AWS RaspberryPi
---

すげー昔にかった日経系のムックについてきた Raspberry Pi の電源をはじめて入れた。

とりあえず、カスタム Linux をSDカードに入れて起動するだけ。とりあえず GPIO の電源と、 GPIO2 でエルチカできることを確認した。まぁー簡単というか、ただの PC のケース向けLEDつけるのと同じぐらいの難易度で、拍子抜け。

AWS IoT (Message Broker)を絡めたデモを作成したいと思っている。

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BGq7nxbkz-8/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">まずエルーピカ</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した写真 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-06-15T09:53:42+00:00">2016 6月 15 2:53午前 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BGq8zGkEzxF/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">かしこくないエルーチカ。まぁできるのはわかった。</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した動画 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-06-15T10:03:59+00:00">2016 6月 15 3:03午前 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## 参考URL

[Raspberry Pi | Device Plus - デバプラ](http://deviceplus.jp/tag/raspberry-pi/)

## 今回買ってきたもの

1,810円(外税)、あと 16G の SD カード750円ぐらい。ラズパイは3000円ぐらいの本についてきたんじゃなかったかなぁ。

USBキーボードは愛用しているこれ → [ぷらっとホーム - Mini Keyboardシリーズ - Mini Keyboard Pro](http://www.plathome.co.jp/products/mini_key/pro/index.html)

電源は昔かったこれ →  [Amazon | Aukey USB 急速 充電器 ACアダプター 50W 6ポート AiPower機能搭載 Apple iPad / iPhone / iPod / Xperia / Nexus / Galaxy等対応 (ホワイト)PA-U14 | AC式充電器 オンライン通販](https://www.amazon.co.jp/gp/product/B00TJJ6Q38/ref=oh_aui_search_detailpage?ie=UTF8&psc=1)

USBマイクロ、HDMIケーブル、LANケーブルは、適当なものを使った。


| 製品                          |  個数 |  値段 |
|:------------------------------|------:|------:|
| 青LED LSLED-B301              |   2個 | 140円 |
| 黄LED LSLED-Y301              |   2個 | 140円 |
| 赤LED LSLED-R301              |   2個 | 140円 |
| ブレッドボード 165408010E     |   1個 | 280円 |
| ブレッドボードワイヤ オスオス |  10本 | 220円 |
| 同オスメス                    |  10本 | 220円 |
| ボタン TVDP01-100-5MM-BK      |  10個 | 220円 |
| 抵抗 1/4W 1kΩ                | 100本 | 270円 |
| 抵抗 1/4W 220Ω               | 100本 | 270円 |
