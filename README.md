# PRICE

PRICE (Probabilistic inference of codon activities by an EM algorithm) is a method to identify ORFs using Ribo-seq experiments embedded in a pipeline for data analysis

#### 1. PRICE is a method to identify ORFs
PRICE is a novel method to identify actively translated codons and ORFs using Ribosome profiling (Ribo-seq) experiments. For this purpose, previously all reads from a specific class (e.g. 29bp long reads) were mapped to the codon at a specific position within the read (e.g. position 12). Classes and positions were determined using genome-wide statistics. PRICE, in contrast, implements a statistical model of the Ribo-seq experiments and infers actively translated codons using maximum likelihood for all reads. Based on the inferred codons, ORF candidates are screened for signatures of active translation using hypothesis tests based on the generalized binomial distribution (which enables to handle complex cases, e.g. of overlapping ORFs).

#### 2. PRICE is full fledged pipeline for Ribo-seq data
PRICE is a software pipeline including all steps necessary to identify and score codons and ORFs starting from one or more fastq files from Ribo-seq experiments. The pipeline includes modules to preprocess (adapter clipping, filtering) and map (Bowtie against transcriptome and genome) sequencing reads, to rescue multimapping reads, to apply the PRICE method to multiple data sets at once and to visualize results (inferred codons and ORFs) using a high-performance genome browser tailored for Ribo-seq data and subsequent integrative analyses.

PRICE is part of [Gedi](https://github.com/erhard-lab/gedi). Source code, [releases](https://github.com/erhard-lab/gedi/releases) and [documentation](https://github.com/erhard-lab/gedi/wiki/Price) can be found in the Gedi repository.
