---
title: "Hidden Markov Models part I : CpG island prediction"
subtitle: "Computational biology"
author: "Jacques van Helden"
date: '2019-11-29'
output:
  slidy_presentation:
    self_contained: false
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    highlight: tango
    incremental: no
    keep_md: yes
    smaller: yes
    theme: cerulean
    toc: yes
    widescreen: yes
  beamer_presentation:
    colortheme: dolphin
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    fonttheme: structurebold
    highlight: tango
    incremental: no
    keep_tex: no
    slide_level: 2
    theme: Montpellier
    toc: yes
  html_document:
    self_contained: false
    fig_caption: yes
    highlight: zenburn
    theme: cerulean
    toc: yes
    toc_depth: 3
    toc_float: yes
  pdf_document:
    fig_caption: yes
    highlight: zenburn
    toc: yes
    toc_depth: 3
  ioslides_presentation:
    self_contained: false
    css: slides.css
    fig_caption: yes
    fig_height: 6
    fig_width: 7
    highlight: tango
    smaller: yes
    toc: yes
    widescreen: yes
  word_document:
    toc: yes
    toc_depth: 3
# font-import: http://fonts.googleapis.com/css?family=Risque
font-family: Garamond
transition: linear
---



## Introduction

During this practical, we will explore different bioinformatics resources to 

- compute Markov models (transition matrices) from different sequence types
- compute the probability of a given sequence with a given Markov models


## Resources

| Resource | Description | URL |
|--------------|---------------------------------|-------------------------|
| UCUS genome Browser | |  [genome.ucsc.edu/](https://genome.ucsc.edu/) |

