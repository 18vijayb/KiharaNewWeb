---
title: "Kihara Lab - Software"
layout: textlay
excerpt: "Software"
sitemap: false
permalink: /software
---

<table class="table table-striped table-hover">
    <thead class="thead-light">
          <tr>
              <th> Name </th>
              <th scope="col"></th>
              <th scope="col">Description</th>
              <th scope="col">Links</th>
          </tr>
    </thead>
    <tbody>
    {% for software in site.data.software %}
        <tr>
            <td class="col">
                {{software.title}}
            </td>
            <td style="text-align:center;width:200px;" valign="top" class="col">
            {% if software.logo %}
            {% assign website_link = software.links | first %}
                <a href="{{website_link.url}}">
                    <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/{{software.logo}}" style="max-width:100%;height:80px;"/> 
                </a>
            {% endif %}
            </td>
            <td class="col">
                {{software.description}}
            </td>
            <td class="col">
                <ul>
                    {% for link in software.links %}
                      <li><a href="{{ link.url }}">{{ link.display }}</a> </li>
                    {% endfor %}
                </ul>
            </td>
        </tr>
    {% endfor %}
    </tbody>
</table>