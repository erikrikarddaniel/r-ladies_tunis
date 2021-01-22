# r-ladies_tunis

Small repo with material from my lecture for R-ladies in Tunis January 2021

## Clone the repository

To get your own local copy of this repository, which includes data and the code I will write
during my lecture, you need to use Git (see https://github.com/git-guides/install-git 
for installation instructions) to clone it:

```bash
git clone https://github.com/erikrikarddaniel/r-ladies_tunis.git
```

## Description of the repository

In the `data` directory there are three tables that we will use:

* `data/samples.tsv`: Data about the samples, primarily dates.

* `data/ampliseq_results/`: This directory was created by [nf-core/ampliseq](https://github.com/nf-core/ampliseq/),
  a pipeline that was used to denoise the data using [DADA2](https://benjjneb.github.io/dada2/index.html)
  and assign taxonomy using [QIIME2's](https://docs.qiime2.org) Bayesian classifier.
  The tables are `ampliseq_results/abundance_table/unfiltered/feature-table.tsv` and
  `ampliseq_results/taxonomy/taxonomy.tsv` for the ASV table and taxonomy tables respectively.
  
* `data/reads/`: Test read files for my Ampliseq demo.
  The classifier I used is available here: https://github.com/nf-core/test-datasets/raw/ampliseq/testdata/GTGYCAGCMGCCGCGGTAA-GGACTACNVGGGTWTCTAAT-gg_13_8-85-qiime2_2019.7-classifier.qza
  (You can use the URL when running the workflow; no need to download the file.)
  I ran this command:
  
```
nextflow run nf-core/ampliseq -r dev -profile docker --manifest data/MANIFEST --classifier https://github.com/nf-core/test-datasets/raw/ampliseq/testdata/GTGYCAGCMGCCGCGGTAA-GGACTACNVGGGTWTCTAAT-gg_13_8-85-qiime2_2019.7-classifier.qza --FW_primer GTGYCAGCMGCCGCGGTAA --RV_primer GGACTACNVGGGTWTCTAAT --max_cpus 2
```
  
In the root directory are the RMarkdowns created before and during the seminar.
