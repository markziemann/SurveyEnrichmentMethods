# SurveyEnrichmentMethods

The purpose of this project is to determine the current state of scientific rigour and reporting standards with respect to functional enrichment studies in the open-access literature.

## Contents

### analysis_code

This is the folder which contains the scripts used to analyse the survey data
and generate charts in Figures 2 and 3.

**analysis1.Rmd** to generate charts shown in Figure 2.

**analysis2.Rmd** to generate charts shown in Figure 3.

**citation_fetching.Rmd** to collect the number of citations for each article considered in the survey.
Do not run this if you are only replicating the generation of the figures as shown in the journal 
article.
Only run this script if you would like to update the number of accumulated citations for the articles 
included in the study.

### data

This folder contains some of the data sets needed to generate the figures as seen in the 
article.

**PMC_2019-analysis.tsv** This is the main spreadsheet including the 1500 articles considered in the
screen.

**QC-analysis.tsv** This is the spreadsheet used for QC analysis, where articles were double and 
triple-checked.

**QC-analysis2.tsv** This is the spreadsheet of articles that underwent double and triple-checking
and where any discrepancies were resolved.
This is required for Figure 2.

**cites_data.rds** This is the citation data as per the journal article required to regenerate the charts
in Figure 3.

**nlmcatalog_result.txt** This required to convert the journal names from pubmed style to the scimago 
style, required for Figure 3.

**scimagojr_2020.csv** This is the table of 2020 Scimago Journal Rankings, required for Figure 3.

### docs

This folder contains some documentation for the project.

**Proposal.md** This is the 1-page proposal for this project.

**manuscript.Rmd** This is the Rmd which is used to generate a working draft of the article and 
demonstrate that the project code is fully reproducible.
The code contained in this document is required to generate Figure 1.

**researcher_guidelines_for_enrichment_analysis.Rmd** This is a set of best practices we have drafted to accompany 
the research article.
These are in draft form and we are seeking additional input from the community to establish authoritative standards.

### examples

This folder contains the scripts required to conduct the analysis of the example RNA-seq datasets 
and generate Figure 4.

**example1-7.Rmd** these scripts contain the code to replicate the analysis of the seven example
RNA-seq datasets. 
The script example1.Rmd is required for Figure 4 panels A-D.

**examples.Rmd** this is a master script used to execute the complete analysis of example datasets 1-7.
It is also required to generate panel E of Figure 4.

### replication

This folder contains some work relating to a pilot replication study, not part of the current manuscript.

## Reproducibility

For the article, we used R version 4.1.
Here is a list of packages loaded.
If you want to rerun this analysis, you have to install the following dependancies from CRAN or Bioconductor.

CRAN: wordcloud, vioplot, reutils, XML, kableExtra, anytime, eulerr, beeswarm, rmdformats, tidyverse, DiagrammeR, DiagrammeRsvg, rsvg.

Bioconductor: getDEE2, DESeq2, clusterProfiler, mitch.

Then git clone this repository and knit the master Rmarkdown.

```
rmarkdown::render("reproduce_analysis_and_manuscript.Rmd")

```
