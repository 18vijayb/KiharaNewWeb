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

<div class="input-group">
<input id="search_table" onkeyup="filterTable()" type="search" class="form-control" placeholder="Search by any keyword" />
</div>
<table id="presentation_table" class="table table-striped table-hover">
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
<script>
    function filterTable() {
    var input, filter, table, tr, td, i, txtValue;
    input = document.getElementById("search_table");
    filter = input.value.toUpperCase();
    table = document.getElementById("presentation_table");
    tr = table.getElementsByTagName("tr");
    for (i = 0; i < tr.length; i++) {
        td = tr[i].getElementsByTagName("td")[1];
        if (td) {
            txtValue = td.textContent || td.innerText;
            if (txtValue.toUpperCase().indexOf(filter) > -1) {
                tr[i].style.display = "";
            } else {
                tr[i].style.display = "none";
            }
        }           
    }
    }
</script>