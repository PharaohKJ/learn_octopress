---
layout: post
title: "フォントを変えた"
date: 2016-09-27 21:08:22 +0900
comments: true
published: true
categories: 
---

おっ。露骨なポスト数稼ぎ! しかしやっぱりピンとこないねー。実はメイリオが一番ピンとくるような…。またウェブフォントを探す旅にでねばならないのかもしれないが、設定がツライんだよな。

```Diff
@@ -1,6 +1,6 @@
  $blockquote: $type-border !default;
 -$sans: "ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro", "メイリオ", Meiryo, "PT Sans", "Helvetica Neue", Arial, sans-serif !default;
 -$serif: "ヒラギノ明朝 Pro W3", "Hiragino Mincho Pro", "PT Serif", Georgia, Times, "Times New Roman", serif !default;
 +$sans: "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", ".HiraKakuInterface-W2", Verdana, "メイリオ", Meiryo, "ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro", "ＭＳ Ｐゴシック", "MS PGothic", sans-serif !default;
 +$serif: Georgia, "ヒラギノ明朝 Pro W3", "Hiragino Mincho Pro", serif !default;
  $mono: Menlo, Monaco, "Andale Mono", "lucida console", "Courier New", monospace !default;
  $heading-font-family: "PT Serif", "Georgia", "Helvetica Neue", Arial, sans-serif !default;
  $header-title-font-family: $heading-font-family !default;
```

さて残りノルマは?

```
~/gitwork/myblog
[pharaohkj]$ ls source/_posts/2016-09*|wc -l
      18
```

今日は9/27(火)、(31件 - 18件) / (31日 - 27日) = 13件 / 4日 = 3.3 件/日。露骨にいくしかねぇ!
