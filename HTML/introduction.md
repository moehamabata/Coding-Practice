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
上下左右の４方向全てではなく、特定のある方向のみに余白を残したい場合は、上記のように「pandding-top: 値;」と記載することでその方向に余白が追加される。下は「pannding-bottom」、右は「pandding-right」、左は「padding-left」となる。

<paddingをまとめて書く>
・個別指定
```html
.logo1 {
   padding-top: 20px;
   padding-right: 10px;
   padding-bottom: 20px;
   padding-left: 10px;
}
```

・省略形①
```html
.logo1 {
  padding: 20px 10px 20px 10px;
}
```
メモ：
値を４つをスペース区切りで指定した場合、「上」「右」「下」「左」の順となる。

・省略形②
```html
.logo1{
   padding: 20px 10px;
}
```
メモ：
値を２つスペース区切りで指定した場合、「上下」「左右」の順となる。

**8. フッターの構造**
<入れ子のセレクタ>
```html
<div class="header-list">
   <ul>
     <li>ヘッダーのリスト</li>
     <li>ヘッダーのリスト</li>
</div>

<div class="footer-list">
  <ul>
    <li>フッターのリスト</li>
  </ul>
</div>
```
メモ：
「.header-list」の後にスペースを空けて「li」と続けると、「header-list」の中の<li>要素のみCSSを適用することができる。
ヘッダーの<li>要素とフッターの<li>要素と、それぞれに別のCSSを適用することが可能。