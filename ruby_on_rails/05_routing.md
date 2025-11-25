## Routingとは
- URLをどのコントローラーアクションに振り分けるかの仕組み全体
- URLと処理を結びつける仕組み
- 
- URLとControllerのアクションを結びつけてくれる
- config/ routes.rbに記載すること
- URLパスに基づいている
- HTTPリクエストを受信している
- Railsの特定コントローラーアクションに対応付けをしている
- URLのリクエストが飛んできた時に、どのコントローラーの、どのアクションにするかを決める場所になる

## Routeとはni
- 

**1. ルーティング確認**
```ruby
Rails.application.routes.draw do
  resources :books
  root 'home#index'
end
```


学んだこと：
- RoutingとRoutesの

気づき・反省：
- RoutingとRoutesの意味が同じだと思っていた。