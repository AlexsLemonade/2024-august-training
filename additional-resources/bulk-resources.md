---
title: Resources for Working with Bulk RNA-seq
---

On this page, we've assembled some resources you may find helpful for working with _bulk transcriptomic data_, include bulk RNA-seq and microarray data.

**Table of contents**

* TOC goes here
{:toc}

## Obtaining practice datasets from `refine.bio`

The Childhood Cancer Data Lab built and maintains [refine.bio](https://www.refine.bio/), a resource of uniformly processed transcriptomic data obtained from publicly available sources.
You can read more about how we process data in refine.bio in [our documentation](http://docs.refine.bio/en/latest/index.html).

If you'd like to practice some of the skills we cover in training or gain some additional ones like making highly customizable heatmaps with the [`ComplexHeatmap`](https://bioconductor.org/packages/release/bioc/html/ComplexHeatmap.html) R package, obtaining processed data from refine.bio is a great starting point.
You may find [our examples for working with data from refine.bio](https://github.com/AlexsLemonade/refinebio-examples) helpful as you look to practice and expand your skills.
In those examples, we use R Notebooks, which you will be familiar with from this workshop!
See the ["Getting Started" section](https://alexslemonade.github.io/refinebio-examples/01-getting-started/getting-started.html) for more information on utilizing our example notebooks.

You can start by searching [refine.bio](https://www.refine.bio/) for keywords relevant to your scientific questions and filtering to the organism and technology (e.g., microarray vs. RNA-seq; refine.bio contains both) you're interested in.

#### Bulk RNA-seq data on refine.bio

The format of the RNA-seq data you can download from the web interface of refine.bio data will be slightly different from what we cover in training.
We summarize our data to the gene-level with `tximport` ([docs](http://docs.refine.bio/en/latest/main_text.html#tximport)), instead of `tximeta` like we do in training, before you download it.
When downloading your data from refine.bio, we recommend checking the box that says "Skip quantile normalization for RNA-seq samples" to obtain the non-quantile normalized data ([docs](http://docs.refine.bio/en/latest/main_text.html#skipping-quantile-normalization-for-rna-seq-experiments)).
You will receive a TSV file that you can use as the counts matrix input for a [`DESeqDataSet`](https://rdrr.io/bioc/DESeq2/man/DESeqDataSet.html).
Note that we recommend using non-quantile normalized data as the `DESeqDataSetFromMatrix()` function requires a counts matrix and not a matrix with normalized or corrected value like TPMs.
See this nice [`DESeq2` vignette](https://bioconductor.org/packages/release/bioc/vignettes/DESeq2/inst/doc/DESeq2.html#count-matrix-input) for more information (Love *et al.*, 2014).
You can read more about using `DESeq2` with refine.bio data [here](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/00-intro-to-rnaseq.html#about-deseq2).

If you identify an RNA-seq experiment from refine.bio that you'd like to use with `DESeq2` (specifically with `DESeqDataSetFromMatrix()`), you can begin by following the instructions in the ["Obtain the dataset from refine.bio"](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html#23_Obtain_the_dataset_from_refinebio) section of any of our RNA-seq refine.bio example notebooks and continue following the steps up until the ["Create a DESeqDataset"](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html#44_Create_a_DESeqDataset) section, as these steps remain pretty much the same across notebooks. Note that you will also need the associated metadata file, which is included in your download in a TSV file that starts with `metadata_`, to create a `DESeqDataSet` object.

#### Microarray data on refine.bio

In this version of our workshop, we won't work with microarray data, but there are hundreds of thousands of microarray samples available from refine.bio.
The microarray datasets you can download from the refine.bio web interface are quantile normalized and are distributed as TSV files you can read into R using functions we cover in training.
The metadata is included in your download in a TSV file that starts with `metadata_`.
You may find our [microarray example notebooks](https://alexslemonade.github.io/refinebio-examples/02-microarray/00-intro-to-microarray.html) for working with refine.bio data helpful with your [differential expression](https://alexslemonade.github.io/refinebio-examples/02-microarray/differential-expression_microarray_01_2-groups.html), [dimension reduction](https://alexslemonade.github.io/refinebio-examples/02-microarray/dimension-reduction_microarray_01_pca.html), or [GSEA pathway analyses](https://alexslemonade.github.io/refinebio-examples/02-microarray/pathway-analysis_microarray_02_gsea.html), to name a few.
Note that our training material is largely RNA-seq specific, so if you obtain microarray data from refine.bio, you should not expect to use the exact same code as we do in training.

## Transcriptome indices for common organisms

We have prepared transcriptome indices for select organisms frequently used in childhood cancer studies including human, mouse, zebrafish, and dog.
Note that for most of files, you will need to perform a few extra steps to read in the quantification data with `tximeta` after performing quantification.
Please see the notebook [`RNA-seq/00c-tximeta_other_species.Rmd`](https://github.com/AlexsLemonade/training-modules/blob/master/RNA-seq/00c-tximeta_other_species.Rmd) for details on how to set this up.

If you have RNA-seq data for an organism that is not listed, please post in the training-specific Slack channel and let your instructors know.

### _Homo sapiens_

Ensembl GRCh38 (hg38) v95

| File description | File use | File path |
|------------------|----------|-----------|
| Human Salmon index `-k 23` | Salmon index for use with `salmon quant`; appropriate for reads shorter than 75bp or for increased sensitivity with `--validateMappings` ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/hg38_cdna/salmon_index/short` |
| Human Salmon index `-k 31` | Salmon index for use with `salmon quant`; appropriate for reads 75bp or longer ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/hg38_cdna/salmon_index/long` |



### _Mus musculus_

Ensembl GRCm38 (mm10) v95

| File description | File use | File path |
|------------------|----------|-----------|
| Mouse Salmon index `-k 23` | Salmon index for use with `salmon quant`; appropriate for reads shorter than 75bp or for increased sensitivity with `--validateMappings` ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/mm10_cdna/salmon_index/short` |
| Mouse Salmon index `-k 31` | Salmon index for use with `salmon quant`; appropriate for reads 75bp or longer ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/mm10_cdna/salmon_index/long` |

### _Danio rerio_

Ensembl GRCz11 v95

| File description | File use | File path |
|------------------|----------|-----------|
| Zebrafish Salmon index `-k 23` | Salmon index for use with `salmon quant`; appropriate for reads shorter than 75bp or for increased sensitivity with `--validateMappings` ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/z11_cdna/salmon_index/short` |
| Zebrafish Salmon index `-k 31` | Salmon index for use with `salmon quant`; appropriate for reads 75bp or longer ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/z11_cdna/salmon_index/long` |

### _Canis lupus familiaris_

Ensembl CanFam3.1 v95

| File description | File use | File path |
|------------------|----------|-----------|
| Dog Salmon index `-k 23` | Salmon index for use with `salmon quant`; appropriate for reads shorter than 75bp or for increased sensitivity with `--validateMappings` ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/CanFam3p1_cdna/salmon_index/short` |
| Dog Salmon index `-k 31` | Salmon index for use with `salmon quant`; appropriate for reads 75bp or longer ([docs](https://salmon.readthedocs.io/en/latest/salmon.html#preparing-transcriptome-indices-mapping-based-mode)) | `~/shared-data/reference/refgenie/CanFam3p1_cdna/salmon_index/long` |
