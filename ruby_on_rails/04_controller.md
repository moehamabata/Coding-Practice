## Controller（コントローラー）
- アプリの司令塔
- ModelとViewの橋渡し役
- 「リクエストを受けて、どのモデルを使って、どのビューを返すか」を決める役割がある

**1. コントローラー作成の基本構文**
```bush
bin/rails generate controller Controller名 アクション1 アクション2...
```
メモ：
- Controller名の後に入力するアクションは複数で指定することが可能
- 作成するには上記のコマンドを使用すること

**2. 全体構造**
```ruby












private

#strong parameters(安全に受け取るための設定)
  def post_params
  parames.require(:post).permit(:tittle,:content)
  end
end
```
メモ：
- PostsControllerは、投稿（Post）に関する処理を担当するクラス

学んだこと：
- 条件分岐やパラメータ処理やエラー処理など、考えるロジックが多く、頭を使う部分でもある

気づき・反省：
- テストをしっかり書かないと、バグが出やすい箇所でもある