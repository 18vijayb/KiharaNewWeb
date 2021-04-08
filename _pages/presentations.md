---
title: "Kihara Lab - Presentations"
layout: piclay
excerpt: "Kihara Lab - Presentations"
permalink: /presentations/
---

# Presentations

## Upcoming Presentations

- 1 oral and 2 poster presentations at 2021 65th Biophysical Society Annual Meeting, February 22-26, 2021
    - (oral) Super resolution cryo-EM maps with 3D generative adversarial networks. Sai Raghavendra Madhuri Venkata Subramaniya, Genki Terashi, & D. Kihara
    - Emap2sec+: Detecting protein and DNA/RNA structures in cryo-EM maps of intermediate resolution using deep learning. Xiao Wang, Eman Alnabati, Tunde Aderinwale, Sai Raghavendra Maddhuri Venkata Subramaniya, Genki Terashi, & D. Kihara
    - VESPER:Global and local cryo-EM map alignment and database search using local density vectors. Genki Terashi, Xusi Han, Charles Christoffer, Siyang Chen, & D. Kihara
- seminar at Butler University, postponed to Fall 2020 or later
- Invited talk at the 4th International Symposium on Cryo-3D Image Analysis 2020, postponed to 2021
- Physical, Computational and Data-driven Biology of Proteins and Nucleic Acids (PCDB2020), Gold Coast, Australia, postponed to 2021
- 2nd Princeton-Nature Conference: Frontiers in Electron Microscopy for the Pysical and Life Sciences, Princeton University, NJ, postponed to 2021
- The Kuntz Symposium, ACS National Fall meeting, postponed to 2021

<table id="publication_table" class="table table-striped table-hover">
    <thead class="thead-light">
        <tr>
            <th scope="col">#</th>
            <th scope="col">Presentation</th>
        </tr>
    </thead>
    <tbody>
        {% assign publication_number = site.data.presentations.size %}
        {% for pres in site.data.presentations %}
            <tr>
                <td class="col">
                    {{publication_number}}
                </td>
                <td class="col">
                    {{ pres.title }}
                    <ul>
                    {% for note in pres.notes %}
                    <li>{{ note }}</li>
                    {% endfor %}
                    </ul>
                </td>
            </tr>
            {% assign publication_number = publication_number | minus: 1 %}
        {% endfor %}
    </tbody>
</table>
