---
title: "Kihara Lab - Home"
layout: homelay
excerpt: "Kihara Lab at Purdue University."
sitemap: false
permalink: /
---

Our research interests lie in the area of bioinformatics. We employ computational methods to elucidate intertwined relationships between protein/gene sequences, structure, function, interactions, genome, and pathways. The ultimate goal of our research projects is to obtain new, comprehensive understanding of how structures and functions are coded in molecular sequences and how functions of molecules are orchestrated in a cell.


<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-pause="hover" >
    <!-- Items -->
    {% assign first = true %}
    <div class="carousel-inner" markdown="0">
        {% for slide in site.static_files %}
        {% if slide.path contains "sliderpic" %}
        {% if first == true %}
        {% assign first = false %}
        <div class=" active item">
        {% else %}
        <div class="item">
        {% endif %}
            <img src="{{ site.url }}{{ site.baseurl }}{{slide.path}}" alt="Slide" />
        </div>
        {% endif %}
        {% endfor %}
    </div>
  <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

Specifically, we develop and apply novel computational methods for...

* Predicting protein structure from sequence
* Predicting protein function from sequence and structure
* Predicting protein-protein and protein-ligand interactions
* Predicting functional sites in sequences
* Genome-scale function and structure annotation
* Analyzing functional units in networks

 **More information can be found on our research projects page [here]({{ site.url }}{{ site.baseurl }}/projects).**

 <div class="row">
  <div class="col-sm-3">
  <a href="https://kiharalab.org/emsuites/index.php">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/EmsuiteLogo.png" style="width: 140px">
  </a>
  Summary Text
  </div>
  <div class="col-sm-3">
  <a href="https://lzerd.kiharalab.org/about/">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/lzerdwebserverlogo.png" style="width: 150px">
  </a>
  Summary Text
  </div>
<div class="col-sm-3" style="vertical-align: bottom;">
  <a href="https://kiharalab.org/3d-surfer/">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/3DSurferLogo.png" style="width: 150px">
  </a>
  Summary Text
  </div>
  <div class="col-sm-2">
  <a href="https://kiharalab.org/em-surfer/">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/emsurferlogo.png" style="width: 150px">
  </a>
  Summary Text
</div>

</div>
 <div class="row">
  <div class="col-sm-3">
  <a href="https://kiharalab.org/proteindocking/">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/lzerdlogo.png" style="width: 150px">
  </a>
  Summary Text
  </div>
<div class="col-sm-3">
  <a href="https://kiharalab.org/esg.php">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/esglogo.png" style="width: 150px">
  </a>
  Summary Text
  </div>
<div class="col-sm-3">
  <a href="https://kiharalab.org/pfp.php">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/pfplogo.png" style="width: 150px">
  </a>
  Summary Text
  </div>
  <div class="col-sm-2">
  <a href="https://kiharalab.org/phylo_pfp.php">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/phylopfplogo.png" style="width: 150px">
  </a>
  Summary Text
  </div>
</div>
