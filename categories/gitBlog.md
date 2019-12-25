---
layout: page
permalink: /blog/categories/gitBlog
title: 깃 블로그
---
 
<h3> Posts by Category : {{ page.title }} </h3>

<div class="card no-margin">
{% for post in site.categories.gitBlog %}
 <li class="category-posts"><span>{{ post.date | date_to_string }}</span> &nbsp; <a class="no-br" href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>