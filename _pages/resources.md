---
title: "Kihara Lab - Resources"
layout: textlay
excerpt: "Kihara Lab - Resources"
sitemap: false
permalink: /resources/
---

# Supplemental Materials from our Publications

{% for resource in site.data.resources %}
- [{{resource.title}}]({{resource.url}})
{% endfor%}