---
layout: post
title: "ブレース2つってJekyllで処理されてしまうん？"
date: 2016-09-22 05:06:07 +0900
comments: true
published: true
categories: 
---

ブレース2つ、全角で書くと `｛｛` をコードブロックに入れたかったんだけどなぜか非表示。

``` html
<li ng-repeat="r in getRecords()"> {{r["k1"]}} {{r["k2"]}} {{r["k3"]}} </li>
```

``` html
<li ng-repeat="r in getRecords()"> {% raw %}{{r["k1"]}} {{r["k2"]}} {{r["k3"]}} {% endraw %}</li>
```

をやりたかったんだ。ああ、LiquidとかJekyllとかかな? 全角で書くと raw プラグインを使って `｛% raw %｝` と `｛% endraw %｝` を使ってエスケープするしかないのかな?
