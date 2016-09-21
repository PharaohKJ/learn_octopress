---
layout: post
title: "AngularJS久しぶりにやる"
date: 2016-09-22 03:18:15 +0900
comments: true
published: true
categories: 
---
    
1.x系。2系とか React はちょっとまだ手を出せていないのでいったんこれで。

## カスタムバリデータ実装

昔は結構苦労したつもりが最近の1系は簡単に実装できるようだ。

[AngularJS: Developer Guide: Forms](https://docs.angularjs.org/guide/forms)

の **Custom Validation** を読めばかんたんにできる。ていうかやりたいことがそのままサンプルとして乗ってる。ていうか、これぐらいのバリデータはデフォで用意してくれよ〜。頼むよ〜。

## ng-if で実行しないようにするとデータに影響

`ng-if` か `ng-show` か `ng-hide` かをちゃんと正しく使わないといけないね。という話。

ていうか、作り的に

- `*.html` が View 
- `*.js` が Model とか Controller 

というつもりで作ると考えてるのに `*.html` の書き方次第でシーケンスが代わってデータに影響あるなんてあきらかに俺の実装が悪いんだろうなー。

## 直接ハッシュをかえすと ng-repeat エラー

ちょっとこれは理由がわからん。ビューはこれ。

``` html
<li ng-repeat="r in getRecords()"> {% raw %}{{r["k1"]}} {{r["k2"]}} {{r["k3"]}} {% endraw %}</li>
```

NGパターン

``` JavaScript
function getRecords() {
    return [
        {"k1":  "v1", "k2":  "v2", "k3":  "v3"},
        {"k1": "v11", "k2": "v22", "k3": "v33"}
    ];
};
```

OKパターン

``` JavaScript
var records = [
    {"k1":  "v1", "k2":  "v2", "k3":  "v3"},
    {"k1": "v11", "k2": "v22", "k3": "v33"},
];

function getRecords() {
    return records;
};
```

何が違うんだ? 


## でかいハッシュをかえしてもエラーる

でかいハッシュをかえすようにして、 `ng-repeat` でまわすと謎死。まず関数実装はこれ

``` JavaScript
var records = [
    {"k1": "v1", "k2": "v2", "k3": "v3"},
    {"k1": "v1", "k2": "v2", "k3": "v3"},
    {"k1": "v1", "k2": "v2", "k3": "v3"},
    {"k1": "v1", "k2": "v2", "k3": "v3"},
    // ... とたくさん
];

function getRecords() {
    return records;
};
```

エラーメッセージは `rootscope infdig apply digest 〜` でデバッグログが埋め尽くされるほどで、まったくピンとこない感じ。

ググるとこれに出会った人はまるでおまじないのようないろいろをやっている模様。まぁデバッグログがうめつくされているのをみると、たぶん、ビューに返しているデータがでかすぎるとおかしいことになってるんじゃないかと予想。メモリが足りないとか、パラメータに食えないとか。

結局まとめてドーンと渡さず、アクセサを作ってそれを用いればなんとかなった

``` JavaScript
var records = [];

function fetchRecords() {
    records = [
        {"k1": "v1", "k2": "v2", "k3": "v3"},
        {"k1": "v1", "k2": "v2", "k3": "v3"},
        {"k1": "v1", "k2": "v2", "k3": "v3"},
        {"k1": "v1", "k2": "v2", "k3": "v3"},
        // .... とたくさん
    ];
};

function getRecord(index) { return records[index]; };
```

こんな感じ。数字を指定してループするのがイマイチピンとこなかったんだが、なんだか `track by` っていうのあるらしい。もうちょっとこのあたり読み込まないとな。

[AngularJS: API: ngRepeat](https://docs.angularjs.org/api/ng/directive/ngRepeat)


## VisualStudioCode for macOS

素晴らしい。何にもカスタムなしで JavaScript + HTML サクサクかけるよ。マジオススメ。

