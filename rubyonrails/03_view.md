## Viewとは
- ユーザーに表示される画面部分
- HTML + ERB（Embedded Ruby）で構成される

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