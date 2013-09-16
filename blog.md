---
layout: page
title : Blog
header : Blog
group: navigation
---
{% include JB/setup %}

#Blog Posts

<ul class="posts">
{% for post in site.posts %}
    {% if post.categories contains 'blog' %}
        <li><span>{{ post.date | date_to_string }}</span><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>