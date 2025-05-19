---
title: アルバム
layout: default
---

# アルバム

イベントや活動の写真集を時系列で掲載します。

<ul class="album-list">
  {% assign albums = site.posts | where_exp: "post", "post.categories contains 'album'" %}
  {% for post in albums %}
    <li>
      <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a><br>
      <span style="font-size:0.95em;color:#888;">{{ post.date | date: "%Y年%m月%d日" }}</span>
      <div>{{ post.excerpt }}</div>
    </li>
  {% endfor %}
</ul>
