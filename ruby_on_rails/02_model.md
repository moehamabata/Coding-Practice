## Model(モデル)

**1. Modelとは**
- データベースとのやり取りや、システムの処理(ビジネスロジック)などを司る機能
- データベースから情報を取り出したり、書き込む際はModevに対して指示を与える

**2. modelコマンドの基本構文**
```rubyonrails
rails generate model Post tittle:string content:text
```
メモ：
- これで、app/models/post.rbが作成される
- tittle - 投稿のタイトル名
- content - 本文