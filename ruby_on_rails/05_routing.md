## Routingとは
- URLとコントローラのアクションを紐づける仕組み

**1. 例**
```rubyonrails
Rails.application.routes.draw do
  resources :books
  root 'home#index'
end
```