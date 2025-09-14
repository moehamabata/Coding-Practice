### レイアウト

**1. ボックスモデル**
- CSSレイアウトの基本中の基本
  
```css
.box {
  width: 200px;
  height: 100px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
  box-sizing: border-box;
}
```

メモ：
- content/padding/border/marginの関係
- 幅・高さの指定（width, height）
- box-sizingの違い（content-box/border-box）

**2. displayプロパティ**

**3. positionプロパティ**
```css
.box {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

メモ：
- static → デフォルト（普通に文書の流れ）
- relative → 元の位置を基準にずらす
- absolute → 親要素を基準に絶対配置
- fixed → 画面に固定
- sticky → スクロールに応じて固定もしくは解除