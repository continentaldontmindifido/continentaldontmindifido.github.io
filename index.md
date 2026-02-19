---
layout: default
title: Continental
---

# Blog Posts

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.date | date: "%B %d, %Y" }}</p>
    {{ post.excerpt }}
  </article>
{% endfor %}
