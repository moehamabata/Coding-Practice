## HTMLの基礎的な使い方

- 見出し（h1~h6）を使ってタイトルをつける
- 段落（p）を使って文章をまとめる
- リンク（aタグ）や画像（imgタグ）の挿入の練習

## 気づき・反省

- タグの入れ子を間違えやすいので注意が必要
- imgタグのalt属性をつけ忘れることがあった
- 実際に書いてみると理解が深まる
- シンプルな自己紹介ページの作成もして、より理解を深めたい

### HTML・CSSの基本的な要素

**1. HTMLバージョンを指定する**

```html
<!-- DOCTYPE宣言を追加してください -->
<!DOCTYPE html>
```

メモ:
・HTMLを記述する際にはDOCTYPE宣言を行う。

**2. htmlの基本的な要素**
```html
<!-- <html>要素を追加してください -->
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

メモ:
・HTMLの基本はDOCTYPE宣言
・htmlの中に、要素としてheader、body、footerなどがある


**3. レイアウト指定**

①文字コード
```html
<!-- 文字コードを「utf-8」にしてください -->
    <meta charset="utf-8">
```

メモ：
・文字コードの指定に用いられる
・また、指定することで文字化けを防ぐことができる
・UTF-1は、HTMLで推奨されている文字コードである


②タイトル指定
```html
<!-- タイトルを「Progate」にしてください -->
    <title>Progate</title>
```

メモ：
・ページのタイトルの設定に用いられる
・指定されたタイトルは、ブラウザのタブ上に現れる。


③CSSの読み込み
```html
<!-- 「stylesheet.css」を読み込んでください -->
    <link rel="stylesheet" href="stylesheet.css">
```

メモ：
・HTMLからCSSを読み込むために必要なもの
・href属性で読み込んだCSSファイルを指定するss


**4. レイアウト**

- レイアウトは<div>要素によって構成されている
- <div>要素のdivは、「division」の略
- 要素をグループ化するために使用される

```html
ヘッダーの<div>要素
<div class="header">
</div>
```

```html
メインの<div>要素
<div class="main">
</div>
```

```html
フッターの<div>要素
<div class="futter">
</div>
```

**5. リストのマークをなくす**

```html
/* list-styleプロパティを用いて、<li>要素の黒点を取り除いてください */
li {
  list-style: none;
}
```

メモ：
<li>リストにlist-styleプロパティを用いてnoneを指定すると、リストの先端のマークを消すことができる。


**６. 横並びにする方法**
```html
li {
  list-style: none;

  /* floatプロパティをleftにしてください */
  float: left;
}
```
メモ：
floatプロパティを使用することで、指定した要素を横並びにすることが可能。

```html
<ul>
  <li>HTML</li>
  <li>PHP</li>
  <li>Ruby</li>
</ul>
```
メモ：
float: left;を指定することで、上記のように要素を左から並べることができる。

**7. ヘッダーの余白。余白の調整**
```html
.logo1 {
    pandding: 20px;
}
```
メモ：
・要素に余白を作る際は、paddingを使用する。
・"padding 値" にすることで上下左右各方面に余白が追加される仕様になっている。

```html
.logo1 {
    pandding-top: 20px;
}
```
メモ：
上下左右の４方向全てではなく、特定のある方向のみに余白を残したい場合は、上記のように「pandding-top: 値;」と記載することでその方向に余白が追加される。