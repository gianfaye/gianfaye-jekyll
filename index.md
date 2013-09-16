---
layout: page
title: "Gian Faye Paguirigan"
tagline: 
---
{% include JB/setup %}
{% include themes/geekyll/about.html %}

<ul class="posts">
  {% for post in site.posts %}
    <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
      <br><span>{{ post.date | date_to_string }}</span></li>
  {% endfor %}
</ul>

Hey, thanks for checking out... The development of this website is still ongoing so you might want to check it again later. In the meantime, you can contact me using the links on the iceberg below.
