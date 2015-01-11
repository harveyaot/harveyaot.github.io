---
layout: page
title: Archive
---

### Thoughts Posts
{% for post in site.categories.thoughts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
