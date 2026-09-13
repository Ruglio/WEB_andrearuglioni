```{=html}
<div class="pub-list">
<% for (const item of items) { %>
  <div class="pub-item">
    <div class="pub-title"><a href="<%= item.outputHref %>"><%= item.title %></a></div>
    <div class="pub-authors"><%= item.author %></div>
    <div class="pub-venue"><%= item.subtitle %></div>
    <% if (item.pdf || item.code || item.slides || item.poster) { %>
    <div class="pub-links">
      <% if (item.pdf) { %><a href="<%= item.pdf %>">PDF</a><% } %>
      <% if (item.code) { %><a href="<%= item.code %>">Code</a><% } %>
      <% if (item.slides) { %><a href="<%= item.slides %>">Slides</a><% } %>
      <% if (item.poster) { %><a href="<%= item.poster %>">Poster</a><% } %>
    </div>
    <% } %>
  </div>
<% } %>
</div>
```
