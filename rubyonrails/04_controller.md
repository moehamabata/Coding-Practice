## Controller（コントローラー）
- 指令や指示を司る機能のこと
- データベースのやり取りや、ブラウザへの反映は、Controller→ModelもしくはViewに命令を与えて実行される
- ユンバーに返すデータを決定する処理を担当する

**1. コントローラー作成の基本構文**
```rubyonrails
bin/rails generate controller Controller名 アクション1 アクション2...
メモ：
- Controller名の後に入力するアクションは複数指定できる
- 作成するには上記のコマンドを使用する
```

```rubyonrails
>_コンソール
Running via Spring preloader in process 18774
      create  app/controllers/grapes_controller.rb
       route  get 'grapes/action2'
       route  get 'grapes/action1'
      invoke  erb
      create    app/views/grapes
      create    app/views/grapes/action1.html.erb
      create    app/views/grapes/action2.html.erb
      invoke  test_unit
      create    test/controllers/grapes_controller_test.rb
      invoke  helper
      create    app/helpers/grapes_helper.rb
      invoke    test_unit
      invoke  assets
      invoke    coffee
      create      app/assets/javascripts/grapes.coffee
      invoke    scss
      create      app/assets/stylesheets/grapes.scss
```
作成されたファイル：
- app/controllers/grapes_controller.rb (Controllerファイル)
- config/routes.rb (ルーティングファイル)
- app/views/grapes/action1.html.erb, app/views/grapes/action2.html.erb (Viewファイル)
- test/controllers/grapes_controller_test.rb (test用ファイル)
- app/helpers/grapes_helper.rb (独自helper設定用のファイル)
- app/assets/javascripts/grapes.coffee (coffeescript)
- app/assets/stylesheets/grapes.scss (scss)

**2. Controllerの命名規則について**
- Modelと結びつきがある場合は、Controller名をGrapesのように複数形にする。
- Railsでは、使用するファイルなどを名前によって自動的に推測するため、命名規則に従っていないと予期しないエラーが発生してしまう。

**3. Controllerを削除する**
```rubyonrails
bin/rails destroy controller Controller名
```

メモ：
- Controller（＋基本的なViewやルーティング）を削除するには、上記のコマンドを使用する

```rubyonrails
bin/rails destroy controller Oranges
```

```rubyonrails
>_コンソール
Running via Spring preloader in process 19022
      remove  app/controllers/grapes_controller.rb
      invoke  erb
      remove    app/views/grapes
      invoke  test_unit
      remove    test/controllers/grapes_controller_test.rb
      invoke  helper
      remove    app/helpers/grapes_helper.rb
      invoke    test_unit
      invoke  assets
      invoke    coffee
      remove      app/assets/javascripts/grapes.coffee
      invoke    scss
      remove      app/assets/stylesheets/grapes.scss
```
メモ：
- rails generate controllerコマンドで作成されたファイルが削除される
- ここで、config/routes.rbに設定されたルーティングの設定は残っていることに注意する
- config/routes.rbには、他のControllerのアクションに関するルーティングも記述されているため、ファイルを削除すると問題になるため

**4. config/routes.rbを編集します**
```rubyonrails
Rails.application.routes.draw do
  get 'grapes/action1'

  get 'grapes/action2'

  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html
end
```

```rubyonrails
>_編集後
Rails.application.routes.draw do
  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html
end
```