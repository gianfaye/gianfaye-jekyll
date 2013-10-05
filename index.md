---
layout: page
title: "Gian Faye Paguirigan"
tagline: 
---
{% include JB/setup %}
{% include themes/geekyll/about.html %}
{% include themes/geekyll/projects-home.html %}

<br />

##Blog Posts
<ul class="posts" style="clear:both;">
  {% for post in site.categories.blog %}
    <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
      <span>{{ post.date | date_to_string }}</span></li>
  {% endfor %}
</ul>