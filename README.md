## Computational Biology

This site contains the teaching material for the course [**Computational Biology**](https://formations.univ-amu.fr/ME5SIN-S51IN1Z4-en.html) taught in the 1st year of the Master [*Computational and Mathematical Biology*](https://formations.univ-amu.fr/ME5SBI-PRSBI5AA-en.html) at [Aix-Marseille Université](https://www.univ-amu.fr/). 

### Links

| Doc | URL | 
|-------------------|------------------------------------------|
| Web site (git pages) | <https://jvanheld.github.io/cmb-comp-bio/> |
| Github repo | <https://github.com/jvanheld/cmb-comp-bio/> |
| [19-20] Computational Biology on Ametice | <https://ametice.univ-amu.fr/course/view.php?id=51934> |

### Teachers

1. Laurent Pezard
2. Michael Kopp
3. Jacques van Helden

### Target audience

- This course is conceived to be followed by a mixed audience of students having a background in either biology or mathematics. 
- Biological and mathematical concepts will thus be introduced progressively. 
- For the practicals, students will be encouraged to form interdisciplinary teams (1 biologist + 1 mathematician) in order to combine their respective skills. 

### Sequence analysis (Jacques van Helden)

Note: The first course (sequence similarity search) partly overlaps with the introductory courses of bioinformatics taught in Life Science Bachelor programs. However, the practical will go a bit further than what has been taught in bachelor. 

1. The practical will rely on a command-line use of the BLAST algorithm, with options specifically tuned to collect a family of proteins from the full proteome of an organism of interest.
2. The practical will also introduce the way to run the analyses on a computer cluster (IFB core cluster), by sending them to a job scheduler (slurm). 

| Session | Date | Topics | Type | Teaching material |
|---|----------|----------------------------------|--------|------------|
| 1 | 2019-11-25 | ¨**Using the IFB NNCR cluster infrastructure** |
| | | Introduction                            | Course     | Slides [[html](slides/01_NNCR-working-environment.html)] [[Rmd](https://raw.githubusercontent.com/jvanheld/cmb-comp-bio/master/slides/01_NNCR-working-environment.Rmd)] |
| | | IFB high performance computing usage | Practical | Slides [[html](https://ifb-elixirfr.gitlab.io/cluster/trainings/slurm/ebai2019.html)] |
| | | First steps with the IFB HPC cluster | Practical | - [IFB cluster doc](https://ifb-elixirfr.gitlab.io/cluster/doc/)<br>- [Quick start](https://ifb-elixirfr.gitlab.io/cluster/doc/quick-start/) <br>- [Slurm user guide](https://ifb-elixirfr.gitlab.io/cluster/doc/slurm_user_guide/) |
| 2  | 2019-11-25 | **Collecting sequence families by sequence alignement**      |
| | | Background concepts for sequence analysis | Course     | [[Slides](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.00.concepts.pdf)] |
| | | Pairwise sequence alignments      | Course     | [[Slides](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.02.pairwise_alignment_slides.pdf)] |
| | | Sequence search by similarity      | Course     | [[Slides](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.03.similarity_searches_slides.pdf)] |
| | | Collecting sequence families with BLAST | Practical  | [[html](practicals/blast_proteome/blast_protein-family.html)][[Rmd](https://raw.githubusercontent.com/jvanheld/cmb-comp-bio/master/practicals/blast_proteome/blast_protein-family.Rmd)] |
| 3 | 2019-11-29 | **Segmenting sequences with HMMs** |
| | | Hidden Markov Models (HMMs)             | Course     | [[Slides](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.05.Hidden-Markov-Models.pdf)] [[Recording](https://amupod.univ-amu.fr/video/3301-applications-of-hidden-markov-models-to-annotate-biological-sequences/)] (requires AMU login) |
| |  | Analysing CpG islands with Markov models        | Practical  | [[html](practicals/markov-models/markov-models.html)] [[Rmd](https://raw.githubusercontent.com/jvanheld/cmb-comp-bio/master/practicals/markov-models/markov-models.Rmd)] |
| 4 | 2019-12-11 |  Analysing CpG islands with Markov models | Solutions (beginning)| [[html](practicals/markov-models/markov-models_solutions.html)] [[Rmd](https://raw.githubusercontent.com/jvanheld/cmb-comp-bio/master/practicals/markov-models/markov-models_solutions.Rmd)] |
|  | | Home work: detecting CpG islands in genomic sequences |  | |


<!--
| 4 | 2019-12-11 | **Detecting protein domains with HMMs** |
| | | Protein domains                         | Course     |  |
| | | Multiple sequence alignments and sequence motifs | Course     | [[Slides](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.04.multiple_alignments_slides.pdf)] |
| | | Detecting protein domains with HMMs     | Practical  |  |
-->

## IFB computing infrastructure

For the practicals, we will use the IFB core cluster, which currently contains 4300 cores adn 400TB storage. 

**Attention**: all tasks must **imperatively** run via the `slurm` task scheduler (never run them on the login node). 

| Resource | URL | 
|------------------------|----------------------------------|
| IFB NNCR cluster: info + account request | https://www.france-bioinformatique.fr/en/cluster |
| Slides: using the IFB core cluster |  https://ifb-elixirfr.gitlab.io/cluster/trainings/slurm/ebai2019.html#1 |
| IFB cluster doc | https://ifb-elixirfr.gitlab.io/cluster/doc/<br>- [Quick start](https://ifb-elixirfr.gitlab.io/cluster/doc/quick-start/) <br>- [Slurm user guide](https://ifb-elixirfr.gitlab.io/cluster/doc/slurm_user_guide/) | 


## Bioinformatics resources used for this course

| Resource | Description | URL | 
|-------|----------------------------------|-------------------|
| **Ensembl** | Genome database | [www.ensembl.org](http://www.ensembl.org/) |
| **UniprotKB** | Knowledge base of protein sequence and functional information | [www.uniprot.org](https://www.uniprot.org/) | 
| **PFAM** | Database of protein families | [pfam.xfam.org](https://pfam.xfam.org/) |

## Supplementary teaching resources

### Bioinformatics introductory course

Introductory course of bioinformatics, for Bachelor students in biology. 

- [Home page of the course](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro)
- [Pairwise alignments](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.02.pairwise_alignment_slides.pdf): global (Needleman-Wunsch) and local (Smith-Waterman) algorithms using dynamical programming
- [Sequence similarity searches with BLAST](http://pedagogix-tagc.univ-mrs.fr/courses/bioinfo_intro/pdf_files/03.03.similarity_searches_slides.pdf)




