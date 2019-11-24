## Computational Biology

This site contains the teaching material for the course [**Computational Biology**](https://formations.univ-amu.fr/ME5SIN-S51IN1Z4-en.html) taught in the 1st year of the Master [*Computational and Mathematical Biology*](https://formations.univ-amu.fr/ME5SBI-PRSBI5AA-en.html) at [Aix-Marseille Université](https://www.univ-amu.fr/). 

### Links

| Doc | URL | 
|-------------------|------------------------------------------|
| Github repo | <https://github.com/jvanheld/cmb-comp-bio/> |
| Git pages | <https://jvanheld.github.io/cmb-comp-bio/> |
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
|--------|----------------------------------|-------------|--------------|
| 1 | 2019-11-25 | ¨**Using the IFB NNCR cluster infrastructure** |
| | | Introduction                            | Course     | Slides [[html](slides/01_NNCR-working-environment.html)] [[Rmd](slides/01_NNCR-working-environment.Rmd)] |
| | | IFB high performance computing usage | Practical | Slides [[html](https://ifb-elixirfr.gitlab.io/cluster/trainings/slurm/ebai2019.html)] |
| | | First steps with the IFB HPC cluster | Practical | - [IFB cluster doc](https://ifb-elixirfr.gitlab.io/cluster/doc/)<br>- [Quick start](https://ifb-elixirfr.gitlab.io/cluster/doc/quick-start/) <br>- [Slurm user guide](https://ifb-elixirfr.gitlab.io/cluster/doc/slurm_user_guide/) |
| 2  | 2019-11-25 | **Collecting sequence families by sequence alignement**      |
| | | Sequence search by similarity      | Course     |  |
| | | Collecting sequence families with BLAST | Practical  | [[html](practicals/blast_proteome/blast_protein-family.html)][[Rmd](practicals/blast_proteome/blast_protein-family.Rmd)] |
| 3 | 2019-11-29 | **Segmenting sequences with HMMs** |
| | | Hidden Markov models                    | Course     |  |
| |  | Annotating CpG islands with HMMs        | Practical  |  |
| 4 | 2019-12-05 | **Detecting protein domains with HMMs** |
| | | Protein domains                         | Course     |  |
| | | Detecting protein domains with HMMs     | Practical  |  |



## IFB computing infrastructure

For the practicals, we will use the IFB core cluster, which currently contains 4300 cores adn 400TB storage. 

**Attention**: all tasks must **imperatively** run via the `slurm` task scheduler (never run them on the login node). 


| Resource | URL | 
|------------------------|----------------------------------|
| IFB NNCR cluster: info + account request | https://www.france-bioinformatique.fr/en/cluster |
| Slides: IFB high performance computing usage |  https://ifb-elixirfr.gitlab.io/cluster/trainings/slurm/ebai2019.html#1 |
| IFB cluster doc | https://ifb-elixirfr.gitlab.io/cluster/doc/<br>- [Quick start](https://ifb-elixirfr.gitlab.io/cluster/doc/quick-start/) <br>- [Slurm user guide](https://ifb-elixirfr.gitlab.io/cluster/doc/slurm_user_guide/) | 


## Bioinformatics resources used for this course

| Resource | Description | URL | 
|-------|----------------------------------|-------------------|
| **Ensembl** | Genome database | [www.ensembl.org](http://www.ensembl.org/) |
| **UniprotKB** | Knowledge base of protein sequence and functional information | [www.uniprot.org](https://www.uniprot.org/) | 
| **PFAM** | Database of protein families | [pfam.xfam.org](https://pfam.xfam.org/) |

