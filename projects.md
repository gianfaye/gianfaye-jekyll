---
layout: page
title : Projects
header : Projects
---
{% include JB/setup %}

# Projects

<p>These are some of my old projects that are not under NDA and can be shared publicly.</p>

## Web
<ul class="posts">
{% for post in site.posts %}
    {% if post.categories contains 'project' and post.tags contains 'web development' %}
        <li><span>{{ post.date | date: "%B %Y" }}</span><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>

## Print
<ul class="posts">
{% for post in site.posts %}
    {% if post.categories contains 'project' and post.tags contains 'print' %}
        <li><span>{{ post.date | date: "%B %Y" }}</span><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>
<br/>

## Software
<ul class="posts">
{% for post in site.posts %}
    {% if post.categories contains 'project' and post.tags contains 'software development' %}
        <li><span>{{ post.date | date: "%B %Y" }}</span><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
{% endfor %}
</ul>