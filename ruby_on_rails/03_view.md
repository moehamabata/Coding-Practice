## Viewとは
- MVCの一つ。Vにあたる
- 画面表示を担当
- HTML + ERB（Embedded Ruby）で構成される
- erbもしくはslimというテンプレートエンジンを使用する

**1. 作成例**
```bush
<!-- app/views/books/index.html.erb -->
<h1>Books一覧</h1>
<ul>
  <% @books.each do |book| %>
    <li><%= book.title %> - <%= book.published %></li>
  <% end %>
</ul>
```

メモ：
- <%= %>：Rubyのコードの実行結果として出力 → 出力結果をHTMLに出力させる
- <% %>：Rubyのコードとして実行　→ 条件分岐(if)、繰り返し(each文)などの制御文記に使われる

学んだこと：
- <%= %>と<% %>の違い。分かっていそうで分かっていなかった

気づき・反省：
- テンプレートはHTMLを生成するファイルであり、Railsのコードを埋め込むことが可能