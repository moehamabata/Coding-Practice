## Model(モデル)

**1. Modelとは**
メモ：
- データベースとのやり取りや、システムの処理(ビジネスロジック)などを司る機能
- データベースから情報を取り出したり、書き込む際はModevに対して指示を与える

**2. modelコマンドの基本構文**
```rubyonrails
rails generate model name field: type[...]
```

**3. 端末を起動する**
```rubyonrails
cd app/sanma/model_demo/
bin/rails generate model book tittle: string published:date sales:bigint rank:integer director:references
```

```rubyonrails
>_コンソール
Running via Spring preloader in process 3683
      invoke  active_record
      create    db/migrate/20180705061405_create_movies.rb
      create    app/models/movie.rb
      invoke    test_unit
      create      test/models/movie_test.rb
      create      test/fixtures/movies.yml
```

メモ：
【db/migrate 20180705061405_create_movies.rb】
（マイグレーションファイル)
- データベース（テーブル）の作成方法を記述したファイルです。ファイル名の先頭の数字部分は、コマンドを実行した日時により異なります。
```rubyonrails
class CreateMovies < ActiveRecord::Migration[5.1]
  def change
    create_table :movies do |t|
      t.string :title
      t.date :published
      t.bigint :sales
      t.integer :rank
      t.references :director, foreign_key: true

      t.timestamps
    end
  end
end
```

【app/models/movie.rb】
(モデルクラスファイル)
- モデルクラスを定義するファイルです。
```rubyonrails
class Movie < ApplicationRecord
  belongs_to :director
end
```

【test/fixtures/movies.yml】
(フィクスチャファイル)
- データベース（テーブル）に格納するデータを記述するファイルです。
```rubyonrails
# Read about fixtures at http://api.rubyonrails.org/classes/ActiveRecord/FixtureSet.html

one:
  title: MyString
  published: 2018-07-05
  sales:
  rank: 1
  director: one

two:
  title: MyString
  published: 2018-07-05
  sales:
  rank: 1
  director: two
```