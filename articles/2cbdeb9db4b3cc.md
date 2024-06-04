---
title: "GASで環境変数(スクリプトプロパティ)を使う方法"
emoji: "🐥"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [GoogleAppsScript]
published: true
---

GoogleAppsScriptでデプロイをするとき、  
デフォルトでライブラリに公開されてしまうため、  
APIキーやパスワードなどを第三者に見られてしまう可能性があります。  
いかんせん怖かったので何か方法が無いかと調べていたところ、  
スクリプトプロパティというのを知ったので設定方法を残しておきたいと思います。  
旧エディタから新エディタに変わったときにGUIからの設定が消えたということだったので、  
結構苦労するのではと思ったのですが、  
ちゃんと存在していました。

# 設定の流れ

![](/images/script_property_click_here.png)
エディタ画面左下の"歯車"マークをクリックします  

![](/images/script_property_2.png)
プロジェクトの設定に移動したら下へスクロールします

![](/images/script_property_3.png)
数字の順番にクリックor入力をしていきます

# 呼び出し方

```js
function getVal() {
  console.log(PropertiesService.getScriptProperties().getProperty("API_KEY"));
}
```
このようにすると”API_KEY”というプロパティに入力されている”値”を参照できます。  
可読性も上がるのでおすすめです。
