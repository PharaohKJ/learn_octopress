---
layout: post
title: "30秒から0.2秒へ！isolateとintegrateとscssのマップファイル作成"
date: 2017-11-06 11:11:57 +0900
comments: true
published: true
categories: life
---

そもそもRakeタスクを眺めていたらそれっぽいのがあった。ページの生成が遅いことは承知なので最新記事だけをプレビューし

- 残りは退避しておけ（`rake isolate`）
- 公開時に戻せ（`rake integrate`）

というのがあるやないか。とりあえずRakefileをいじって俺好みにした。さてこれでどれぐらいの速度でできるのか。

```
 ...done in 7.660925 seconds.
```

んー、オーダーが足りん。せめて1秒台になってもらわんと…

ていうか遅いのは本当に記事作成か？　とちょっと真面目に調べてみたらどうやらscssのmapファイル作成が遅いように思えてきた。ていうか `config.rb` では `sourcemap = true` 行はコメントアウトしてあるしなあ。もしかして何か前回CSSデバッグしたとき **設定の** キャッシュがきいてしまって毎度出力してしまっているのでは？ `ls -l ./public/stylesheets/screen.css.map` してタイムスタンプを確認すると明らかに毎度作成している。

`# sourcemap = true` を `sourcemap = false` と明示的に指定してみたらビンゴで

```
[pharaohkj]$ be rake generate
## Generating Site with Jekyll
 modified config.rb
    clean source/stylesheets
   delete source/stylesheets/screen.css
    write source/stylesheets/screen.css
Configuration file: _config.yml
Configuration file: _amazon.yml
            Source: source
       Destination: public/
      Generating...
                    done.
```

その結果、これは早い！

```
...done in 0.198859 seconds.
```

30秒から0.2秒。99.3％はSCSSのコンパイル+マップ作成だったのか？　検証のためisolateをやめてみたらやっぱり23秒ぐらい（`...done in 22.667441 seconds.`）かかった。結局記事がたくさんあるとサイト生成遅いのは変わらない。固定して7秒ぐらいがSCSS+マップ作成にかかる時間のようだ。isolate使っていこう。
