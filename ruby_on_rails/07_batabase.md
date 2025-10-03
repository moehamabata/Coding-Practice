**1. DB操作**
- マイグレーション、モデル、シードデータで管理

**2. マイグレーション例**
```rubyonrails
rails generate migration AddPublishedToBooks published:date
rails db:migrate

3. seeds.rb 例

Book.create(title: "Rails入門", published: "2025-01-01")
```