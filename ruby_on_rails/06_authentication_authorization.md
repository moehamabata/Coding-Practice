**1. Authentication（認証）**
- ユーザーのログイン・ログアウト管理
- Devise を使うのが一般的

**2. Authorization（認可）**
- 誰がどの機能を使えるかの権限管理
- Pundit や CanCanCan を使用する

```rubyonrails
# Pundit例
class PostPolicy < ApplicationPolicy
  def update?
    user.admin? || record.user_id == user.id
  end
end
```