---
layout: page
title : Projects
header : Projects
---
{% include JB/setup %}

#Projects

##Web
<ul class="posts">
{% for post in site.posts %}
    {% if post.categories contains 'projects' and post.tags contains 'web development' %}
        <li><span>{{ post.date | date: "%B %Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>

##Print
<ul class="posts">
{% for post in site.posts %}
    {% if post.categories contains 'projects' and post.tags contains 'print' %}
        <li><span>{{ post.date | date: "%B %Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>