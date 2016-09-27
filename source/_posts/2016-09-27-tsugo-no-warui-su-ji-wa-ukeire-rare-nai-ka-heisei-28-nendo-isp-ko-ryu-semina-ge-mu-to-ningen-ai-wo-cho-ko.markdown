---
layout: post
title: "都合の悪い数字は受け入れられないのか - 『平成28年度ISP交流セミナー ゲームと人間とAI』を聴講"
date: 2016-09-27 22:22:14 +0900
comments: true
published: true
categories: 
---

いろいろあって

[DGnet - <講演会>平成28年度ISP交流セミナー　ゲーム と 人間 と AI(人工知能)　～ 北陸先端大「エンタテインメント科学センター」のご紹介 ～ - （公財）石川県産業創出支援機構（ISICO）](http://www.isico.or.jp/dgnet/eventseminar/40622)

を聴講した。もう「ゲームはコリゴリ」という気持ちはあったが、まぁAIが学べるならいいかな、ぐらいの気持ち。

## マシーンのような男

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">弱いことが人間らしい。超強くなったら人間も機械も近づいていく。だから、超強くなってしまったものをうまく弱くすることが「人間らしさ」を出せるのではないかという仮定。</p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/780639508156981249">2016年9月27日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


## ゲーム洗練度理論

ゲーム理論に加えていかにエキサイティングできるかを加えた数字。これでクソゲーかどうか判定できるんじゃないかという話。流行ってるスポーツ、トラディショナルボドゲ(チェス、麻雀、など)の統計をとると同じぐらいのスコアになるので、ゲームデザインに活かせそう。ていうかこれ入力して回答がでるツールは売り物になるんじゃないかなあ?

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">JAIST Repository: ゲーム洗練度の理論: サッカーとチェスの比較 <a href="https://t.co/QBCfgsjJ2P">https://t.co/QBCfgsjJ2P</a> <a href="https://t.co/Yrj2KIHMEz">https://t.co/Yrj2KIHMEz</a></p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/780642830515511296">2016年9月27日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


## 都合の悪い数字は受け入れられない

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">サイコロで自分に不利な値がでると「目を操作している！！！！！」と人間は勘違いする。なので「非常にうまく目を操作してユーザーの気持ちいい乱数を機械学習で作る」。サンプルゲームがカルドセプトでおもしろいうえに、闇が見える。見える。</p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/780656208919212032">2016年9月27日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">コンピュターで作った擬似乱数を人間にみせると「これは乱数じゃないと思う」、人間が想像で作った乱数ぽい数字一覧を人間にみせると「これは乱数だと思う」。だと。</p>&mdash; ふぁらお加藤 (@PharaohKJ) <a href="https://twitter.com/PharaohKJ/status/780657090792529920">2016年9月27日</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

これは本当に興味深い話だ。そして「実は『わからないように』目が操作されてる」てのは恐ろしい話だ。

結局、人間は「そんなはずはないだろう」というものは受け入れられないのだ。例えば前職で

- 誰がどうみても「数字の1」
- だけど、AIが特徴抽出しOCRの結果として出したのは「数字の8」であった

こういうことがおこった場合、お客様や営業からクレームがきたりしていた。「間違えるわけないだろ」と。

しかし、この字を拡大すると、

- かすれて1の線に穴がぼこぼこ空いている
- 穴が2つあるといえば数字の8しかない

ので、8である。それでも「納得できない。なんとかしてほしい」というので、特徴の取り方を調整したところ、次は誰が見ても「8」が「1」になるのである。そりゃそーだ。

結局、OCRエンジンを作っているチームから言えば「どんなデータでもなるべく正答率をあげる」のが仕事であるが、営業さんは「サンプル帳票の正答率を 100％ にして売る」のが仕事である立場の違いだ。しかもそうやって営業さんがパラメータ調整すればするほど本番の正答率は下がってしまっていると予想できる。とても難しい問題だった。

これはほんと、今の機械学習とかでもそうで「ええっ? これは間違いじゃないのか?」という結果がでたとしても、その数字が受け入れられるかどうかというのは別問題なのだ。本当にこれはAIをやる上でとても難しい。バグか仕様かがわからんのだ。

JAWS-UGで某展示員としゃべったときもそうだった。「我々は機械学習によって結果は出しますが、その結果に納得できないと言われても困りますし、望む結果がでるにはどうしたらいいのか? など業務改善案を出したりすることはできない」と100度ぐらいおっしゃっていた。これはそういうクレーム多いんだろうなと予想する。

会の締めで「結局『人間とAIを分ける』のは結果に対する責任をとる覚悟だ」と言われていた。確かに、機械には「出世」「立場」「背景」などなどなどといった、不純物が一切ない代わりに掛ける覚悟はない。やはりAIとなると一気に哲学的なところに話が及ぶなあ。
