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
  
In the root directory are the RMarkdown(s) created during the seminar.
