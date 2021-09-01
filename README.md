# SurveyEnrichmentMethods

The purpose of this project is to determine the current state of scientific rigour and reporting standards with respect to functional enrichment studies in the open-access literature.

## Contents

**Proposal.md** This is the projects 1 page proposal.

**example.Rmd** This is an example of what the results look like when ORA is misused. Figure 1.

**analysis.Rmd** This is the large dataset analysis that starts with 1500 articles.
The latter part of this is the basis for Figure 4.

**QC_analysis.Rmd** This is a smaller dataset analysis for 200 articles that were double-checked.

**QC_analysis2.Rmd** This is a smaller dataset analysis for 200 articles that were double-checked after resolving the discrepancies.
This is the basis for Figure 3.

**citation_fetching.Rmd** This script shows the citation numbers were obtained for the articles.

**cites_data.rds** This dataset contains the citation data.
Because this runs very slowly, we provide it as a static dataset.

**manuscript_draft.Rmd** This is an Rmd which is a draft form of the manuscript. It also contains code for generating Figure 2.

**data** This folder contains the survey datasets.

**images** folder for saving the png and pdf images. Currently contains pngs of the figures.

## Reproducibility

For the article, we used R version 4.1.
Here is a list of packages loaded.
If you want to rerun this analysis, you have to download these from CRAN or Bioconductor.

Biobase
clusterProfiler
DESeq2
DiagrammeR
DiagrammeRsvg
eulerr
getDEE2
kableExtra
mitch
RColorBrewer
reutils
rsvg
tidyverse
vioplot
wordcloud
wordcloud2
XML

Then git clone this repository and run the Rmds in the following order:

1. QC_analysis2.Rmd

2. analysis.Rmd

3. manuscript_draft.Rmd
