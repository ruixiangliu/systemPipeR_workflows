# systemPipeR_Workflows

This is a repository that provides several versions of [_systemPipeR_](http://www.bioconductor.org/packages/devel/bioc/html/systemPipeR.html) workflows.


## systemPipeR: NGS workflow and report generation environment 

[_systemPipeR_](http://www.bioconductor.org/packages/devel/bioc/html/systemPipeR.html)
is an R/Bioconductor package for building and running automated *end-to-end*
analysis workflows for a wide range of next generation sequence (NGS)
applications such as RNA-Seq, ChIP-Seq, VAR-Seq and Ribo-Seq. Important
features include a uniform workflow interface across different NGS applications, automated
report generation, and support for running both R and command-line software,
such as NGS aligners or peak/variant callers, on local computers or compute
clusters. The latter supports interactive job submissions and batch submissions
to queuing systems of clusters. Efficient handling of complex sample sets and
experimental designs is facilitated by a well-defined sample annotation
infrastructure which improves reproducibility and user-friendliness of many
typical analysis workflows in the NGS area.

#### Installation 
To install the _systemPipeR_ package, please use the _`BiocManager::install`_ command:

```
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::install("systemPipeR")
```
To install the _systemPipeRdata_ package, please use the _`BiocManager::install`_ command:

```
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::install("systemPipeRdata")
```

To obtain the most recent updates immediately, one can install it directly from Bioconductor or GitHub as follow:

```
# Bioconductor
BiocManager::install("systemPipeR", version = "3.9")
BiocManager::install("systemPipeRdata", version = "3.9")

# GitHub
BiocManager::install("tgirke/systemPipeR", build_vignettes=TRUE, dependencies=TRUE)
BiocManager::install("tgirke/systemPipeRdata", build_vignettes=TRUE, dependencies=TRUE)
```

#### Usage
Instructions for running _systemPipeR_ are given in its main
[_vignette_](https://htmlpreview.github.io/?https://github.com/tgirke/systemPipeR/blob/master/inst/extdata/vignette_archive/systemPipeR.html) (manual).
The sample data set used in the vignette are provided by the data package [_systemPipeRdata_](https://github.com/tgirke/systemPipeRdata).
The expected format to define NGS samples (_e.g._ FASTQ files) and their
labels are given in
[_targets.txt_](https://github.com/tgirke/systemPipeR/blob/master/inst/extdata/targets.txt)
and
[_targetsPE.txt_](https://github.com/tgirke/systemPipeR/blob/master/inst/extdata/targetsPE.txt)
(latter is for PE reads).
The run parameters of command-line software are defined by param files that
have a simplified JSON-like name/value structure. Here is a sample param file
for _Tophat2_:
[_tophat.param_](https://github.com/tgirke/systemPipeR/blob/master/inst/extdata/tophat.param).
Templates for setting up custom project reports are provided by [_systemPipeRdata_](https://github.com/tgirke/systemPipeRdata).
The corresponding PDFs of these report templates are linked here:
[systemPipeRNAseq](https://htmlpreview.github.io/?https://github.com/tgirke/systemPipeRdata/blob/master/inst/extdata/workflows/rnaseq/systemPipeRNAseq.html),
[systemPipeRIBOseq](https://htmlpreview.github.io/?https://github.com/tgirke/systemPipeRdata/blob/master/inst/extdata/workflows/riboseq/systemPipeRIBOseq.html),
[systemPipeChIPseq](https://htmlpreview.github.io/?https://github.com/tgirke/systemPipeRdata/blob/master/inst/extdata/workflows/chipseq/systemPipeChIPseq.html)
and
[systemPipeVARseq](https://htmlpreview.github.io/?https://github.com/tgirke/systemPipeRdata/blob/master/inst/extdata/workflows/varseq/systemPipeVARseq.html).

#### Slides
+ [Overview Slide Show](https://htmlpreview.github.io/?https://github.com/tgirke/systemPipeR/blob/master/inst/extdata/slides/systemPipeRslides.html).



