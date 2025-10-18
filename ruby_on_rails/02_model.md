## Model(モデル)

**1. Modelとは**
- MVCの一つ。Mにあたる
- データベースとのやり取りや、システムの処理(ビジネスロジック)などを
- データベースから情報を取り出したり、書き込む際はModelに対して指示を与える

**2. modelコマンドの基本構文**
```bash
rails generate model Post tittle:string content:text
```
メモ：
- これでapp/models/post.rbが作成される
- tittle - 投稿のタイトル名
- content - 本文

**3. RailsアプリのPostモデルに関するテストを実行する**
```bash
bundle exec rspec spec/models/post_spec.rb
```
メモ：
- bundle exec : Gemfileに書かれたRubyのライブラリ（Gem）を使ってコマンドを実行する
- RailsやRspecのバージョンはアプリごとに異なる場合がある
- 上記のことから、bundle execをつけることで「このプロジェクトのRspecを使うように」と指示を出している


学んだこと：Gemfile
- Modelコマンドを打つことでtittleとcontentのカラムを持つ

気づき・反省：
- ここでの"post"はデータの設計図であり、Rubyで動く。「投稿」というデータをRubyの世界で扱うための設計書です。
- Modelの役割は幅広いが、書き込む時はModelが指示を出すというとことではないので認識違いが起こらないようにしておく