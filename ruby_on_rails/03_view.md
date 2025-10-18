## Viewとは
- MVCの一つ。Vにあたる
- 画面表示を担当
- HTML + ERB（Embedded Ruby）で構成される
- erbもしくはslimというテンプレートエンジンを使用する

**1. 作成例**
```rubyonrails
<!-- app/views/books/index.html.erb -->
<h1>Books一覧</h1>
<ul>
  <% @books.each do |book| %>
    <li><%= book.title %> - <%= book.published %></li>
  <% end %>
</ul>
```

メモ：
- <% %>はRubyのコードとして実行
- <%= %>はRubyのコードの実行結果を出力

学んだこと：
- 

気づき・反省：
- テンプレートはHTMLを生成するファイルであり、Railsのコードを埋め込むことが可能