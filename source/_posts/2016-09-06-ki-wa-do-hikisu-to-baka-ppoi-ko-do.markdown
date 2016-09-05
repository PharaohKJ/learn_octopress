---
layout: post
title: "キーワード引数のバカっぽいコードと引数評価順序"
date: 2016-09-06 02:22:12 +0900
comments: true
published: true
categories: 
---

キーワード引数、名前付き引数(C# ではこう呼ぶらしく、英語では Named Arguments らしい)がなにやらいろんな言語で採用されるらしいが、私も Ruby 2系で「コレいいかもな」と思った仕組みである。

例えば、四角の面積を求める関数があったとして C++ ならば関数定義に `int 面積(int width, int height);` とし、呼び出し側では `area = 面積(10, 30);` としてあっても、どっちが幅( `width` )で、どっちが高さ( `height` )なのか区別がピンとこない。(サンプルが悪くてどっちでもいいじゃんてのは置いておいて)

これがキーワード引数だと、まぁちょっと仮想言語記述だが呼び出し時に

```
area = 面積(width: 10, height: 30);
```

とかけるので、ピンとくる。

キーワード引数なしでも似たようなことはできて、

```
width  = 10;
height = 30;

area = 面積(width, height);
```

とまぁ、キーワード引数なしでもとても読みやすく、書きやすく書ける。それにほとんどの場合は以下のように「どこかの関数」「メンバで持つ値」などを用いるので、これを小さいスコープの変数に取り込んだほうがコンパイラ最適化などもきいていい。

```
width  = GUI.InputValues['Width'].Text.toInt();
height = GUI.InputValues['Height'].Text.toInt();

area = 面積(width, height);
```

さて、これをキーワード引数で書くと

```
width  = GUI.InputValues['Width'].Text.toInt();
height = GUI.InputValues['Height'].Text.toInt();

area = 面積(width: width, height: height);
```

になってしまい、 `width: width, height: height` あたりがとてつもなくバカっぽい。かしこいフリをして以下のようにかく。

```
area = 面積(
    width:  GUI.InputValues['Width'].Text.toInt(),
    height: GUI.InputValues['Height'].Text.toInt()
);
```

これはいい感じだ。

```
area = 面積(
    GUI.InputValues['Width'].Text.toInt(),
    GUI.InputValues['Height'].Text.toInt()
);
```

これよりも読みやすい。ステキだ。

こうなってくると次は「関数に渡す引数一覧の評価順序はどうなってるんだ？」というのが気になってくる。パラメータで指定できるので、引数の順序は意味をもたず、呼び出す側の気まぐれな順序でも問題ないからだ。

みなさんご存知のように古いC言語やC++では、 **引数の評価順序は未定義で実装依存** であり「左から右に実行されている」のは直感、たまたまにすぎない。( `a = a + 1` と書いて、右辺から評価されることは直感的に受け入れられるよう訓練しても、関数に指定した引数の最後から評価されることは直感的に受け入れられないよな。)

昔のVisualC++では、その関数の [呼出規約](https://ja.wikipedia.org/wiki/%E5%91%BC%E5%87%BA%E8%A6%8F%E7%B4%84)のスタックに積む順番で呼ばれていたような記憶がある。

つまり、ある日コンパイラオプションをかえたりすると、呼び出される順序が変わるというツラサ。まぁこのツラサは C11、C++11 ではちゃんと定義された。ていうかこんなことでツラミを感じるのはコードが悪いというのはおっしゃるとおり。そして、お仕事でC11以降が使えるかどうかはまた別だしね。

Java、Python、Ruby、JavaScript(ECMAScript)、PHPは左から右と決まってるので安心していい。

んん? 呼び出しの順なのかそれとも定義時の順なのか気になる。Rubyぐらいは試しておくか。

```
def area(param1: 0, param2: 0)
end

def func1
  p 'func1'
end

def func2
  p 'func2'
end

area(param1: func1, param2: func2)
area(param2: func2, param1: func1)
```

結果

```
irb(main):013:0* area(param1: func1, param2: func2) # 関数定義は 1 -> 2、呼び出しも 1 -> 2
"func1"
"func2"
=> nil
irb(main):014:0> area(param2: func2, param1: func1) # 関数定義は 1 -> 2、呼び出しは 2 -> 1
"func2"
"func1"
=> nil
```

ちゃんと呼び出し側の直感であろう期待通りだ。安心した。

