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
```html

メモ：
・文字コードの指定に用いられる
・また、指定することで文字化けを防ぐことができる
・UTF-1は、HTMLで推奨されている文字コードである


②タイトル指定
```html
<!-- タイトルを「Progate」にしてください -->
    <title>Progate</title>
```html

メモ：
・ページのタイトルの設定に用いられる
・指定されたタイトルは、ブラウザのタブ上に現れる。


③CSSの読み込み
```html
<!-- 「stylesheet.css」を読み込んでください -->
    <link rel="stylesheet" href="stylesheet.css">
```html

メモ：
・HTMLからCSSを読み込むために必要なもの
・href属性で読み込んだCSSファイルを指定するss


**4. レイアウト**

- レイアウトは<div>要素によって構成されている
- <div>要素のdivは、「division」の略
- 要素をグループ化するために使用される

```ヘッダーの<div>要素
<div class="header">
</div>

```メインの<div>要素
<div class="main">
</div>

```フッターの<div>要素
<div class="futter">
</div>

**4. ヘッダーの枠組み**