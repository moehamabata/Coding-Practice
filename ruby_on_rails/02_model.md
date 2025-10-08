## Model(モデル)

**1. Modelとは**
- データベースとのやり取りや、システムの処理(ビジネスロジック)などを司る機能
- データベースから情報を取り出したり、書き込む際はModelに対して指示を与える

**2. modelコマンドの基本構文**
```bash
rails generate model Post tittle:string content:text
```
メモ：
- これでpostテーブルが作成される
- tittle - 投稿のタイトル名
- content - 本文

学んだこと：
- Modelコマンドを打つことでtittleとcontentのカラムを持つ

気づき・反省：
- Modelの役割は幅広いが、書き込む時はModelが指示を出すというとことではないので認識違いが起こらないようにしておく