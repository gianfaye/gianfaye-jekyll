---
layout: page
title: "Gian Faye Paguirigan"
tagline: 
---
{% include JB/setup %}
{% include themes/geekyll/about.html %}
{% include themes/geekyll/projects-home.html %}

<br />

<ul class="posts" id="blog-home" style="clear:both;">
  {% for post in site.categories.blog %}
    {% if post.tags contains 'featured' %}
    	<li><a href="{{ BASE_PATH }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
      <span>{{ post.date | date_to_string }}</span></li>
    {% endif %}
  {% endfor %}
</ul>
<div class="view-all">
    <a href="/posts">&lt; View all blog posts &gt;</a>
</div>