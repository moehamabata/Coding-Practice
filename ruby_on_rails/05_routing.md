## Routingとは
- URLパスに基づいている
- HTTPリクエストを受信している
- Railsの特定コントローラーアクションに対応付けをしている
- URLが飛んできた時に、どのコントローラーの、どのアクションを決めるかの場所でもある

**1. ルーティング確認**
```ruby
Rails.application.routes.draw do
  resources :books
  root 'home#index'
end
```