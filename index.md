---
layout: default
title: Home
---

# Latest Posts

{% for post in site.posts limit: 10 %}
<div class="post">
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
  {{ post.excerpt | strip_html | truncate: 250 }}
</div>
{% endfor %}

{% if site.posts.size == 0 %}
<p>No posts published yet. Add new Markdown files to the `_posts` folder to get started!</p>
{% endif %}
