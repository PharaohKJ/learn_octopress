---
layout: post
title: "デジタルデバイドの先をハックできるのか？そして、獣害・耕作放棄地について考える『Code for Kanazawa Civic Hack Night vol.13』に参加"
date: 2016-06-10 10:25:37 +0900
comments: true
published: true
categories: civichack
---

CfK の CHN に参加した。

[Code for Kanazawa Civic Hack Night Vol.13 - Code for Kanazawa | Doorkeeper](https://codeforkanazawa.doorkeeper.jp/events/46358)

といっても、 [codeforkanazawa-org/ha4go: ha4go](https://github.com/codeforkanazawa-org/ha4go) の開発打ち合わせがメインで、他は話半分にきいていた。

隣の席が「獣害」「耕作放棄地」についての話題がでていた。話半分な要旨をまとめると

- とにかく「畑などに人がおらず、メンテされていない」
- 「メンテされていない」となると獣害はますますひどくなる
- 「ひどいと放棄せざるをえない」つまり、スパイラル
- とにかく、無料でもいいから人にきて耕作・畑作して、メンテしてほしい
- ただし、「無料でもいい」といっている方々は端末の操作などは期待できない

ということのようにきこえた。獣害の問題については、また専門的な議論が必要だとして、ここで私が考えた大きなテーマは「デジタルデバイド・情報格差で分離されてしまっている端末も操作できない方々をハックできるのか？」である。

ならば「端末も操作できないような方々向けのアプリ・装置」が必要だとすると、これはかなりの作り込みが必要になる。つまり「無料であげるから」どころか「金を払ってあげるから」ぐらいが本当は必要となる。

結局、「使えない」のコストを誰が払うか？の問題に帰結する。

「お年寄りがスマフォを使えない」と「しょうがないね」。という気持ちになり、「今の若者はスマフォばかりでPCが使えない」と「勉強不足だ」。という気持ちになるのはまともなセンスか？気持ちや育った背景などわからなくもないが、これは差別的な話だ。できるやつはできるし、できないやつはできない。よって、この問題は弱者側のコストをどうサポートするか？というのが、いわゆる「Civic Hack」では、どのような問題だろうが確実についてまわる問題であろう。

しかもこのような「みなで団結してやらねばならぬ」「できない人間は不便な生活のままでどうぞ」で住む問題ではない場合、やはり、行政やボランティアなど、「運用」の世界になってしまうんじゃないかなぁ・・・。

しかし、こういう相談を誰にお願いすればいいのか？とっかかりをもとめてCHKにきていただけたのはすばらしいね。行政に行かないのは残念かもしれないが。


## 普通に考えたらマッチングサービス？

あと、単純に耕作地マッチングサービスなどを作ればよいと考えるがその運用は地獄の体をなすだろうなぁと想像してしまう。例えばこんな感じ

- 無料！ということで謎のボット・業社・個人が登録してまわる
- 謎がこられると困るので、マッチングサービスが個人情報を要求せざるをえなくなる
- まぁ土地が絡むからしょうがないだろうということで役所との連携もいる
- 外国の人とかどうすんの？
- そもそもタダで貸してるのにこない！
- マッチングした人が気に入らない！

そういうわけで、形としては「耕作放棄地」をオープンデータとして収集(自治体か、国かが提供)、そこにオファーがかけられるサイト、ぐらいがバランスとれてるのじゃないか？


## 文化・土壌の構築

最近、BBQ料理にハマって、いろいろ見ているが、スパイス業社やソース業社が調理法コンテンツを提供しているのを見ると、「文化・土壌を作る」というところからやってるなぁーと感心する。キューピーマヨネーズ3分クッキングとかもまさにそれだ。

なので、直接利用者に金を払うかはおいておいて、「田舎の耕作地を貸し出してて、それをパッと検索して、好きなところ選んで、そこで農業やってみてはどう？地元の人がサポートするよ」ぐらいの文化・土壌を「金をかけて構築」せねばならぬだろうなぁと考えた。


## 夕食

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BGdQHJXEzza/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">特濃最高。汁がなくなるまで替え玉した。</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">ふぁらお加藤さん(@pharaohkj)が投稿した写真 - <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-06-10T02:23:22+00:00">2016 6月 9 7:23午後 PDT</time></p></div></blockquote> <script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
