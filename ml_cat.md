---
layout: page
title: Archive
---

## Machine Learning Posts
{% for cat in site.categories %}
{% if cat == 'ml' %}
<h2>{{ category | first }}</h2>
</span>{{ category | last | size }}</span>
    {% for post in category.last %}
        *{{ post.date | date:"%d/%m/%Y"}}  &raquo; [{{ post.tile }}] ({{ post.url }})
{% endif %}
{% endfor %}
