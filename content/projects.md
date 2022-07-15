+++
title = "Projects"
slug = "projects"
+++

## [Lorikeet](https://rhysnewell.github.io/Lorikeet/)
![](/images/lorikeet_logo.png)

Lorikeet is a variant calling, strain genome resolving, and microdiversity assessment algorithm for metagenomics.
The variant calling algorithm Lorikeet uses is a full re-implementation of the GATK HaplotypeCaller algorithm
in Rust. It is both faster and easier to use with almost identical results. Lorikeet can make use of both long and short
reads simultaneously, handling both the mapping and parallelization of the analysis of multiple genomes with minimal effort
required of the user.

## [Rosella](https://rhysnewell.github.io/rosella/)
![](/images/rosella.png)

Rosella is a metagenomic binning algorithm written in Rust and Python. It makes use of UMAP and HDBSCAN to generate
metagenomic assembled genomes from metagenome assemblies. It can both map and calculate coverage information for assemblies
and is capable of handling and long and short reads simultaneously.

## [Aviary](https://rhysnewell.github.io/aviary/)
![](/images/aviary_logo.png)

Aviary is a modular and easy to use to complete metagenomic workflow written in python wrapping around snakemake. Aviary 
is capable of handling hybrid assembly of long and short reads from various sequencing platforms. Additionally, Aviary performs
robust binning using a large suite of metagenomic binners and ensemble binning. Finalized bins are also assessed for quality using
CheckM, and assigned taxonomic ranks using GTDB-tk. Various other statistics are also reports like recovered diversity at various steps
using [SingleM](https://github.com/wwood/singlem) and coverage statistics using [CoverM](https://github.com/coverm)


## [ChIP-R](https://github.com/rhysnewell/chip-r)

ChIP-R is a reproducibility assessment algorithm for ChIP-seq and ATAC-seq data. It allows the testing of multiple replicates at a time
allowing users to generate finalized sets of high confidence ChIP-seq and ATAC-seq peaks with ease. The publication can be found
[here](https://www.sciencedirect.com/science/article/abs/pii/S0888754321001531)

## Contributions

- [Kingfisher](https://github.com/wwood/kingfisher-download)
- [CoverM](https://github.com/wwood/coverm)
- [Galah](https://github.com/wwood/galah)

## Hobby side projects 
### Nymph
Non-negative matrix factorization in rust
