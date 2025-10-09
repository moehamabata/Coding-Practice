## Routingとは
- URLとコントローラのアクションを紐づける仕組み

**1. ルーティング確認**
```ruby
Rails.application.routes.draw do
  resources :books
  root 'home#index'
end
```