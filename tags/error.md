---
layout: page
permalink: /blog/tags/error
title: "#Error 디버그"
---
 
<h3> Posts by Tags : {{ page.title }} </h3>

<div class="card no-margin">
{% assign tags = site.tags %}
{% for category in tags %}
    {% assign postList = category[1] %}
    {% assign categoryInfo = category[0] %}
    {% for category in categoryInfo %}
        {% assign tagUrl = category[0] %}
        {% assign tagName = category[1] %} 
        {% if tagUrl == 'error' %}
            {% for post in postList %}
                <li class="category-posts"><span>{{ post.date | date_to_string }}</span> &nbsp; <a class="no-br" href="{{ post.url }}">{{ post.title }}</a></li>
            {% endfor %}
        {% endif %}
    {% endfor %}
{% endfor %}
</div>