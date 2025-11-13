## Controller（コントローラー）
- MVCの一つ。Cにあたる
- アプリの司令塔
- 「リクエストを受けて、どのモデルを使って、どのビューを返すか」を決める役割がある
- 条件分岐やパラメータ処理やエラー処理など、考えるロジックが多く、頭を使う部分でもある
- テストをしっかり書かないと、バグが出やすい箇所でもある

**1. コントローラー作成の基本構文**
```bush
bin/rails generate controller Controller名 アクション1 アクション2...
```
メモ：
- Controller名の後に入力するアクションは複数で指定することが可能
- 作成するには上記のコマンドを使用する

**2. 全体構造**
```ruby
class PostController < ApplicationController
#投稿一覧を表示する
def index
  @posts=Post.all
end

#新規投稿フォームを表示する
def new
  @post=Post.new
end

#新しい投稿をデータベースを保存する
def create
  @post=Post.new(post_params)
  if @post.save
    redirect_to root_path
  else
    render :new
  end
end

private

#strong parameters(安全に受け取るための設定)
  def post_params
  parames.require(:post).permit(:tittle,:content)
  end
end
```
メモ：
- PostsControllerは、投稿（Post）に関する処理を担当するクラス