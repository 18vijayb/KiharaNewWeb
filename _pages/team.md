---
title: "Kihara Lab - Team"
layout: gridlay
excerpt: "Kihara Lab: Team members"
sitemap: false
permalink: /team/
---

### For information on openings see [here](#openings).

# Group Members

Jump to [staff](#staff), [undergraduate students](#undergraduates), [collaborators](#collaborators), [alumni](#alumni).

<img src="{{ site.url }}{{ site.baseurl }}/images/gallerypic/Aug2019_grouppic.jpg" class="img-responsive" width="95%" style="float: left" />

## Staff
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">
  {% for education in member.education %}
    <li> {{ education.bullet }} </li>
  {% endfor %}
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Undergraduates
{% assign number_printed = 0 %}
{% for member in site.data.undergrad_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">
  {% for education in member.education %}
    <li> {{ education.bullet }} </li>
  {% endfor %}
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Collaborators

 <div>
 <table class="table">
  <tbody>
  {% for member in site.data.collaborators %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.position }} </td>
  <td> {{member.location}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
 </div>

## Alumni

<div id="accordion">
  <div class="card">
  <div class="card-header" id="visitingProfsHeader">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseVisitingProfessors" aria-expanded="false" aria-controls="collapseVisitingProfessors">
    Visiting Professors
  </button>
  </h5>
  </div>
  <div id="collapseVisitingProfessors" class="collapse" aria-labelledby="visitingProfsHeader" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.visiting_professors %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.position }} </td>
  <td> {{ member.university }} </td>
  <td> {{member.dates}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="visitingScholarsHeader">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseVisitingScholars" aria-expanded="false" aria-controls="collapseVisitingScholars">
    Visiting Scholars
  </button>
  </h5>
  </div>
  <div id="collapseVisitingScholars" class="collapse" aria-labelledby="visitingScholarsHeader" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.visiting_scholars %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.university }} </td>
  <td> {{member.dates}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="headingThree">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
    PostDoctoral Fellows
  </button>
  </h5>
  </div>
  <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.postdoctoral_fellows %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.position }} </td>
  <td> {{ member.location }} </td>
  <td> {{member.dates}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="gradStudentsHeader">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseGradStudents" aria-expanded="false" aria-controls="collapseGradStudents">
    Graduate Students
  </button>
  </h5>
  </div>
  <div id="collapseGradStudents" class="collapse" aria-labelledby="gradStudentsHeader" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.graduate_alumni %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.program }} </td>
  <td> {{ member.location }} </td>
  <td> {{member.date}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="otherSupervisedGradHeader">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseOtherSupervisedGrad" aria-expanded="false" aria-controls="collapseOtherSupervisedGrad">
    Other Supervised Graduate Students
  </button>
  </h5>
  </div>
  <div id="collapseOtherSupervisedGrad" class="collapse" aria-labelledby="otherSupervisedGradHeader" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.other_graduate_alumni %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.program }} </td>
  <td> {{member.dates}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="programmersHeader">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseProgrammers" aria-expanded="false" aria-controls="collapseProgrammers">
    Programmers
  </button>
  </h5>
  </div>
  <div id="collapseProgrammers" class="collapse" aria-labelledby="programmersHeader" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.programmers %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.program }} </td>
  <td> {{member.date}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="undergradHeader">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseUndergrads" aria-expanded="false" aria-controls="collapseUndergrads">
    Undergraduate Students
  </button>
  </h5>
  </div>
  <div id="collapseUndergrads" class="collapse" aria-labelledby="undergradHeader" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.undergraduate_alumni %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.program }} </td>
  <td> {{member.dates}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="card-header" id="K12Header">
  <h5 class="mb-0">
  <button class="btn" data-toggle="collapse" data-target="#collapseK12" aria-expanded="false" aria-controls="collapseK12">
    K-12 Students
  </button>
  </h5>
  </div>
  <div id="collapseK12" class="collapse" aria-labelledby="K12Header" data-parent="#accordion">
  <div class="card-body">
  <table class="table">
  <tbody>
  {% for member in site.data.K-12_alumni %}
  <tr>
  <td> {{ member.name }} </td>
  <td> {{ member.school }} </td>
  <td> {{member.date}} </td>
  </tr>
  {% endfor %}
  </tbody>
  </table>
  </div>
  </div>
  </div>
</div>

# Openings

### Postdoctoral Positions

Qualified candidates should hold a PhD in Physics, Computer Science, Biology, Chemistry, Doctor of Engineering, or in a related field. The primary area sought is protein tertiary structure modeling & prediction, protein docking, and protein global/local shape comparison and search. Experience in electron microscopy or tomography data analysis, and 3D shape retrieval are plus. Fluent programming skill and good communication skills are essential. Highly motivated and creative candidates with a strong record of publication are encouraged to apply. Send curriculum vitae and contact information of three references to: dkihara@purdue.edu . Postal mail should be sent to: Dr. Daisuke Kihara, Department of Biological Sciences, Purdue University, Hockmyer Hall of Structural Biology, 249 S. Martin Jischke Drive, West Lafayette, IN 47907.

### Graduate students

Highly motivated graduate students in the departments of computer science, biological sciences, PULSe program at Purdue are encouraged to contact Dr. Kihara. Available projects include protein 3D shape comparison, docking, 3D structure prediction, function prediction, and DNA sequence analyses (motif search, small RNA detection). Please note that usually research assistantship is only offered after working at least one semester as an independent study to prove productivy. Previous experience in bioinformatics is desirable but not necessary. Programming skill is not a requirement at the beginning if you are not CS major as long as you are eager to learn it in the first year.

### Undergraduate Students

If you are interested in computational work in biology, you are almost always welcome to our group. We have worked with over twenty undergraduate students, and have a good record of scientific achievments with them, including publishing full research papers, research presentation in conferences, entering graduate programs. Feel free to contact Dr. Kihara.

### Summer internship with pay

Not offered.