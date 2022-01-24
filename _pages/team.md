---
title: "Kihara Lab - Team"
layout: gridlay
excerpt: "Kihara Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


Jump to [staff](#staff), [master and bachelor students](#master-and-bachelor-students), [alumni](#alumni), [administrative support](#administrative-support), [lab visitors](#lab-visitors).

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

## Undergraduate Students
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