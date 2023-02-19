---
title: "wow.jsとAnimate.cssを使おうとして動かなくてスタックした話"
emoji: "🐥"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [wowjs, Animatecss]
published: true
---

https://web-saku.net/wow-js-and-animate-css-animation/

# Animate.cssのバージョンが4以降の場合はinit()の変更を

```
<script>
wow = new WOW(
    {
        animateClass:   'animaate__animated'
    }
)
wow.init();
</script>
```

Animate.css 4.0以降はclass名が変わったようで  
検索して出てきた結果はだいたいwow.init()するだけ！ばっかりで  
役に立たなかった。

# あとがき
とりあえず無事に動作したので良かった。  
wowのクラス名で判定してスクロールで表示したらanimateClassを追加してる？  
それでアニメーションが動作してるのかな  
なんにせよ、ありがたく使おうと思う。