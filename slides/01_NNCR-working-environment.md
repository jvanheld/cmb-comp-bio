---
title: "Infrastructure and software environment"
subtitle: "IFB National Network of Computing Resources"
author: "Jacques van Helden"
date: '2019-11-28'
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



## Command-line tools in bioinformatics

- A large proportion of bioinformatics tools are available only on the command line. Moreover, even for tools equipped with a graphical user interface (e.g. BLAST, clustal, ...) the use of command-line can be necessary for some projects

- Enables to automate the tasks

    - Managing repetitive processes: apply the same task to numerous data files or with many different options
    - Managing complex processes combining many tasks (workflows)

- High performance computing (HPC)

    - running tasks that require huge resources of computing and storage

- Traceability, reproducibility, reusability

    - traceability: keeping track of each step and parameter used to produce a result 
    - reproducuibility; enabling to re-run the analysis and reproduce the same results
    - reusability: enabling to run the same analysis with different data

## Working environments

Most bioinformatics tools can be installed on Unix-like operating systems (Linux, Mac OS X), and can be used in different environments. 

- Terminal of your own computer (Linux, Mac OS X)
- Virtual Machine (e.g. [VirtualBox](https://www.virtualbox.org/), [VWMare](https://www.vmware.com/))
- Containers ([Docker](https://www.docker.com/), [singularity](https://www.sylabs.io/singularity/))
- Terminal of a remote computer (via an `ssh` connection)
- Bureau Virtuel

## Virtual machines

- Components

    - host: can be your own computer (note: also used to deploy services on HPC computers)
    - host operating system (Linux, Mac, Windows)
    - virtual machine (VM) : emulation of an other computer, that runs on the host machine
    - operating system of the VM: Linux, Windows, ...
    - hypervisor (= monitor): software that runs the virtual machines on the host

- Typical applications

    - run a Linux OS on a Windows or Macintosh PC
    - test a software under different operating systems
    - isolate a service from the host system (security, resource segmentation)

- Examples of hypervisors

    - VirtualBox (<https://www.virtualbox.org/>)
    - VWMare (<https://www.vmware.com/>)


## Container-based virtualisation

- Applications run on a shared operating system without requiring a virtual machine


- Advantages

    - modular combination of applications and libraries ("à la carte")
    - less resource-consuming than virtual machines

- Container management software

    - Docker (<https://www.docker.com/>)
    - singularity (<https://www.sylabs.io/singularity/>)


## Virtual machines versus containers



<div class="figure" style="text-align: center">
<img src="images/vm_vs_container.png" alt="**Comparaison of virtualisation solutions.** Right: Virtual Machine; Center: Docker container; right: Singularity container. Source: Greg Kurtzer keynote at HPC Advisory Council 2017 @ Stanford" width="90%" />
<p class="caption">**Comparaison of virtualisation solutions.** Right: Virtual Machine; Center: Docker container; right: Singularity container. Source: Greg Kurtzer keynote at HPC Advisory Council 2017 @ Stanford</p>
</div>


## Installation of software tools in the local operating system

- Advantages

    - Immediate availability of the tools
    - Direct invocation by the native operating system (more efficient)

- Weaknesses

    - Dependences (system libraries, language libraries, other executables)
    - Incompatibilities between dependences of different tools
    - The installation of some tools and libraries requires admin rights
    - OS-dependency of package managers ([package managers](https://en.wikipedia.org/wiki/Package_manager)): apt-get, yum, ports, brew, ...
    - Some applications and libraries are available only on some package managers. 

## Conda packages

- Doc : <https://conda.io/docs/>

- Advantages

    - A multi-platform package manager (Linux, Mac OS X, Windows)
    - All the installations can be done at the user-level (no need to be admin)
    - Community project supported by a large community (computer scientists, statisticians, bioinformaticians, ...) $\rightarrow$ ever-increasing number of supported tools an libraries 
    - Continuous integration $\rightarrow$ very fast response to requests
    - Very precise management of the dependencies and version
    - Seamingless management of uninstallation for no more required software
    - Trying it is adopting it!

- Weaknesses

    - If each used installs each tool and dependencies in her/his own account, this creates redundancy and waste of storage space.

## Computer cluster

A cluster is a set of computers (denotes as **nodes**) that work together and can be seen as a single system. Clusters are generally used to run parallel computing


<div class="figure" style="text-align: center">
<img src="images/600px-IBM_Blue_Gene_P_supercomputer.jpg" alt="**Grappe de serveurs.** En avant-plan: *Homo sapiens* tentant d'établir une interaction physique avec les machines.  Source: &lt;https://en.wikipedia.org/wiki/Parallel_computing&gt;" width="60%" />
<p class="caption">**Grappe de serveurs.** En avant-plan: *Homo sapiens* tentant d'établir une interaction physique avec les machines.  Source: <https://en.wikipedia.org/wiki/Parallel_computing></p>
</div>


## Parallel computing


Parallel computing consists in running simultaneously a series of processes on a computer system. 

Tasks can be distributed on several Computer Processing Units (**CPUs**) of a same computer and/or on several computers (cluster).

The distribution of tasks on nodes and CPUs relies on a **job scheduler**. Users submit jobs (in the form of command lines or scripts) to the scheduler, which manages their execution on the different nodes and CPUs. 

