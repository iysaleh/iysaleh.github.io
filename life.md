---
title: Life
layout: life
---
<h1 style="text-align:center">Ibraheem's Life</h1>
<h3 style="text-align:center">Well, some of it atleast...in pictures!</h3>

<ul>
{% for file in site.static_files  %}
  {% assign pageurl = page.url | replace: 'index.html', '' %}
  {% if file.path contains pageurl %}
    {% if file.extname == '.jpg' or file.extname == '.jpeg' or file.extname == '.JPG' or file.extname == '.JPEG' %}
<li><a class="lightbox-image" href="{{site.url}}{{ file.path }}"><img loading="lazy" class="lightbox-image" height=640 width=480 src="{{site.url}}{{ file.path }}" /></a></li>
    {% endif %}
  {% endif %}
{% endfor %}
</ul>
