```{=html}
<div class="pub-list">
<% for (const item of items) { %>
  <% const href = item.outputHref.replace(/^publications\//, "") %>
  <% const year = (String(item.date || "").match(/\d{4}/) || [""])[0] %>
  <div class="pub-item">
    <div class="pub-year"><%= year %></div>
    <div class="pub-body">
      <div class="pub-title"><a href="<%= href %>"><%= item.title %></a></div>
      <div class="pub-authors"><%= item.author %></div>
      <% if (item.subtitle) { %><div class="pub-venue"><%= String(item.subtitle || "").replace(/ -- /g, " – ") %></div><% } %>
      <% if (item.pdf || item.code || item.slides || item.poster) { %>
      <div class="pub-links">
        <% if (item.pdf) { %><a href="<%= item.pdf %>">PDF</a><% } %>
        <% if (item.code) { %><a href="<%= item.code %>">Code</a><% } %>
        <% if (item.slides) { %><a href="<%= item.slides %>">Slides</a><% } %>
        <% if (item.poster) { %><a href="<%= item.poster %>">Poster</a><% } %>
      </div>
      <% } %>
    </div>
  </div>
<% } %>
</div>
```
