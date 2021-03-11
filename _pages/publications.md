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
            <th scope="col">Publication Name</th>
            <th scope="col">Access Link</th>
            <th scope="col">Abstract</th>
        </tr>
    </thead>
    <tbody>
        {% assign publication_number = site.data.publist.size %}
        {% for publi in site.data.publist %}
            {% assign is_odd = publication_number | modulo: 2 %}
            <tr>
                <td class="col">
                    {{publication_number}}
                </td>
                <td class="col">
                    {{ publi.title }} {{ publi.authors }}
                </td>
                <td class="col">
                    <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
                </td>
                {% if publi.abstract %}
                <td class="col">
                    <a href="{{ publi.abstract.url }}">{{ publi.abstract.display }}</a>
                </td>
                {% endif %}
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
  }
}
</script>