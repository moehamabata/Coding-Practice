## Routingとは
- URLパスに基づいている
- HTTPリクエストを受信している
- config/ routes.rbが対応箇所
- Railsの特定コントローラーアクションに対応付けをしている
- URLのリクエストが飛んできた時に、どのコントローラーの、どのアクションを決める場所になる


**1. ルーティング確認**
```ruby
Rails.application.routes.draw do
  resources :books
  root 'home#index'
end
```