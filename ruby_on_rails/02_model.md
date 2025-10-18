## Model(モデル)

**1. Modelとは**
- MVCの一つ。Mにあたる
- データベースとのやり取りや、システムの処理などを担当している
- データベースから情報を取り出したり、書き込む際はModelに対して指示を与える

**2. modelコマンドの基本構文**
```bash
rails generate model モデル名
```
メモ：
- こうすることでモデルを作成することができる
```bash
rails g model モデル名
```
メモ：
- 省略してこのようにしてもモデルを作成することができる
```bash
rails generate model Post tittle:string content:text
```
メモ：
- これでapp/models/post.rbが作成される
- tittle - 投稿のタイトル名
- content - 本文
- Modelを作成するときは、１文字目を大文字にする
- 
**3. Modelの作成が成功した際のコマンド**
```bash
```

**4. Modelをデータベースに適用させるためのコマンド**
```bash
bundle exec rspec spec/models/post_spec.rb
```
メモ：
- bundle exec : Gemfileに書かれたRubyのライブラリ（Gem）を使ってコマンドを実行する
- RailsやRspecのバージョンはアプリごとに異なる場合がある
- bundle execをつけることで「このプロジェクトのRspecを使うように」と指示を出している

学んだこと：
- Gemfile：Modelコマンドを打つことでtittleとcontentのカラムを持つ

気づき・反省：
- ここでの"post"はデータの設計図であり、Rubyで動く
- 「投稿」というデータをRubyの世界で扱うための設計書
- Modelの役割は幅広いが、書き込む時はModelが指示を出すというとことではない
- よって、認識違いが起こらないようにしておく