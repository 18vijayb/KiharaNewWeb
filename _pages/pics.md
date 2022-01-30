---
title: "Kihara Lab - Pics"
layout: textlay
excerpt: "Kihara Lab - Pics"
sitemap: false
permalink: /pics
---

#### Gallery
(Right-click *'open image in new tab'* to see a larger image.)
{% assign number_printed = 0 %}
{% for pic in site.static_files %}
{% if pic.path contains "gallerypic" %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}{{pic.path}}" class="img-responsive" width="95%" style="float: left" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}

{% endif %}
{% endfor %}