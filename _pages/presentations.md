---
title: "Kihara Lab - Presentations"
layout: piclay
excerpt: "Kihara Lab - Presentations"
permalink: /presentations/
---

# Presentations

## Upcoming Presentations

<table id="publication_table" class="table table-striped table-hover">
    <thead class="thead-light">
        <tr>
            <th scope="col">#</th>
            <th scope="col">Presentation</th>
            <th scope="col">Relevant Links</th>
        </tr>
    </thead>
    <tbody>
        {% for pres in site.data.upcomingpresentations %}
            <tr>
                <td class="col">
                    {{pres.number}}
                </td>
                <td class="col">
                    {{ pres.text }}
                    <ul>
                    {% for note in pres.notes %}
                    <li>{{ note.text }}</li>
                    {% endfor %}
                    </ul>
                </td>
                <td class="col">
                    {% for link in pres.links %}
                    <a href="{{link.url}}">{{ link.display }}</a>
                    {% endfor %}
                </td>
            </tr>
        {% endfor %}
    </tbody>
</table>

## Past Presentations

<table id="publication_table" class="table table-striped table-hover">
    <thead class="thead-light">
        <tr>
            <th scope="col">#</th>
            <th scope="col">Presentation</th>
            <th scope="col">Relevant Links</th>
        </tr>
    </thead>
    <tbody>
        {% for pres in site.data.presentations %}
            <tr>
                <td class="col">
                    {{pres.number}}
                </td>
                <td class="col">
                    {{ pres.text }}
                    <ul>
                    {% for note in pres.notes %}
                    <li>{{ note.text }}</li>
                    {% endfor %}
                    </ul>
                </td>
                <td class="col">
                    {% for link in pres.links %}
                    <a href="{{link.url}}">{{ link.display }}</a>
                    {% endfor %}
                </td>
            </tr>
        {% endfor %}
    </tbody>
</table>
