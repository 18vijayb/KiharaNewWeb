---
title: "Kihara Lab - Publications"
layout: gridlay
excerpt: "Kihara Lab - Publications"
sitemap: false
permalink: /publications/
---

Publications
------------

<div class="input-group">
<input id="search_table" onkeyup="filterTable()" type="search" class="form-control" placeholder="Search in publications..." />
</div>
<table id="publication_table" class="table table-striped table-hover">
    <thead class="thead-light">
        <tr>
            <th scope="col">#</th>
            <th scope="col">Year</th>
            <th scope="col">Publication Name</th>
            <th scope="col"></th>
            <th scope="col"></th>
            <th scope="col">Relevant Links</th>
        </tr>
    </thead>
    <tbody>
        {% assign publication_number = site.data.publist.size %}
        {% for publi in site.data.publist %}
            {% assign is_odd = publication_number | modulo: 2 %}
            <tr>
                <td class="col">
                    {{publi.number}}
                </td>
                <td class="col">
                    {{publi.year}}
                </td>
                <td class="col">
                    <em>{{ publi.authors }}</em>, <b>{{ publi.title }}</b>
                </td>
                <td class="col">
                {% if publi.link %}
                    {% if publi.link.url contains "paper/" %}
                      <a class="btn btn-primary" href="{{ site.url }}{{ site.baseurl }}/{{ publi.link.url }}">{{ publi.link.display }}</a>
                    {% else %}
                      <a class="btn btn-primary" href="{{ publi.link.url }}">{{ publi.link.display }}</a>
                    {% endif %}
                {% endif %}
                </td>
                <td class="col">
                {% if publi.abstract %}
                  <a class="btn btn-primary" href="{{ publi.abstract.url }}">{{ publi.abstract.display }}</a>
                {% endif %}
                </td>
                <td class="col">
                  {% for link in publi.links %}
                    <a href="{{ link.url }}">{{ link.display }}</a> <br>
                  {% endfor %}
                </td>
            </tr>
            {% assign publication_number = publication_number | minus: 1 %}
        {% endfor %}
    </tbody>
</table>

<script>
function filterTable() {
  var input, filter, table, tr, td, i, txtValue;
  input = document.getElementById("search_table");
  filter = input.value.toUpperCase();
  table = document.getElementById("publication_table");
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
    td = tr[i].getElementsByTagName("td")[2];
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