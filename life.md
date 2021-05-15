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
<li><a class="lightbox-image" href="{{site.url}}{{ file.path }}"><img loading="lazy" class="lightbox-image" src="{{site.url}}{{ file.path }}" /></a></li>
    {% endif %}
    {% if file.extname == '.mp4' or file.extname == '.MP4' %}
<li><a class="lightbox-video" href="{{site.url}}{{ file.path }}"><img src="{{site.url}}/assets/posters/{{file.name}}.jpg" class="lightbox-video" /></a></li>
    {% endif %}
  {% endif %}
{% endfor %}
</ul>
