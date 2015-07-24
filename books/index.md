---
layout: page
title: Books
excerpt: "List of books iOS Developers should read."
---

<ul class="post-list">
{% for post in site.categories.books %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span></a></article></li>
{% endfor %}
</ul>
