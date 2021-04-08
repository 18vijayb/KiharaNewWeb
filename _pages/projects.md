---
title: "Kihara Lab - Projects"
layout: textlay
excerpt: "Kihara Lab - Projects"
sitemap: false
permalink: /projects/
---

# Research Projects

We are working in a very exciting area of protein bioinformatics. We develop various methods and tools for predicting and modeling protein structures, functions, and complexes, which were not able before. In many projects, we use various algorithms and machine leaning methods including deep learning, Conditional Random Field, SVM, random forest, and other methods. 
Below several major projects are briefly summarized. For more information, refer to related papers published by our group (a number in a parenthesis speficies a reference in [the publication page]({{ site.url }}{{ site.baseurl }}/publications)) and also our [software]({{ site.url }}{{ site.baseurl }}/software).

### Protein Structure Modeling for Cryo-EM

Cryo-electron microscopy (cryo-EM) has become a powerful experimental method for solving macromolecular structures. But a challenge is that ofen the resolution of density maps determined is not very high, at medium to low resolution (~ 4 to 10 Angstroms).` We are actively developing computational methods for aiding protein structure modeling from medium to low resolution cryo-EM maps using various algorithms including deep learning. See

- [MAINMAST](https://kiharalab.org/emsuites/mainmast.php)
- [Emap2sec](https://kiharalab.org/emsuites/emap2sec.php)
- [EM-Surfer](https://kiharalab.org/em-surfer/)

and other related publications.

### Protein Docking Prediction

We develop algorithms and sofware to build 3D models of protein-protein interactions. We are continuously participating in CAPRI protein docking assessment and ranked among top. Visit [LZerD protein docking suite](https://kiharalab.org/proteindocking/) and refer to related publications.

### Protein Structure Prediction

Protein tertiary structure provides indispensable information for elucidating protein function and evolution. We are developing computational methods for predicting protein tertiarty structure from sequence [35, 23, 19] and methods for error estimation of computational models [31]. We are actively participating the CASP protein structure prediction assessment. Particularly, we were the top in the novel fold category in CASP11 and among the top in the protein structure refinement category in CASP 12.

### Protein Surface Analysis

Protein surface is where function of a protein realizes. Especially interaction with proteins and chemical compounds occur at a specific site of a protein surface. Hence, finding characteristics sites for protein function, e.g. active sites of enzymes, protein interaction interface, is a promising way to predict function of a protein. The aims of this project include development of methods for protein surface shape comparison for fast database search [34] and characterization of surface geometrical property of proteins [30, 28]. We use a versatile shape descriptor, 3D Zernike descriptors and 2D and 3D Krawchouk moments for this task. We have developed [3D-Surfer](https://kiharalab.org/3d-surfer/) and [EM-Surfer](https://kiharalab.org/em-surfer/), web-based software for fast protein comparison and surface analysis.

We have also revealed how the 3D shapes of proteins and protein complexes distirbute, i.e. 3D protein shape universe. Please check out this cool paper with video clips of the protein shape universe.

### Computational drug screening

Computational pre-screening of drugs can drastically reduce the cost for developing new drugs target proteins. We developed [PL-PatchSurfer](https://kiharalab.org/plps2/), molecular surface-based drug screening tool. We are also actively participating various drug screening contests and achieved successful outcomes. The papers of contests include [174], [166], [136].

### Protein Function Prediction

Function annotation of genes is a foundation of almost any molecular biology studies. Conventional methods for function annotation are homology search methods, such as BLAST and FASTA. These methods perform well when obvious homologs exist for a query protein, but don't provide any functional information otherwise. As a consequence, typically about only half of genes are annotated in a newly sequences genome. For a large scale omics analysis, it is helpful if function annotation coverage is larger even with less specific or low-resolution function [32, 26]. The goal of this project is to develop methods which can predict function to a larger number of genes than conventional homology search by providing low-resolution function when necessary witout losing accuracy. Our method, PFP [22], ESG [43], Phylo-PFP [147], Consensus method won the best prediction method in CASP7 and Automatic Function Prediction Meeting (AFP-SIG, ISMB 2005), and among top ranks in CAFA1, 2, 3. Please try our servers:

- [PFP Website](https://kiharalab.org/web/pfp.php)
- [ESG Website](https://kiharalab.org/web/esg.php)
- [Phylo-PFP Website](https://kiharalab.org/phylo_pfp.php)
- [NaviGO Website](https://kiharalab.org/web/navigo/views/goset.php)

### Theoretical studies of protein folding and evolution

We are also very interested in physical and information theoretic nature of protein folding and protein sequence-structure-complex-function relationships. If interested, please refer to [104].

### Sequence Analysis of Intergenic Regions of Genomes

Intergenic regions contain important information for gene regulation. In recent years various families of small non-coding RNAs (sRNAs) have been discovered both in bacterial and eukaryotic genomes. We have developed an ensemble approach of DNA motif discovery, which outperforms standalone programs [24, 20]. We have also computationally identified sRNAs in 30 bacterial genomes and conducted comparative study [27].