# Proposal: Reproducibility and rigour of published functional enrichment studies

Lead Investigator: TBA

Supervisor: Mark Ziemann

## Background

Gene set enrichment analyses are a widely used and powerful class of analytical tools for summarising omics data [1](Khatri et al, 2012).
Despite this, when performed improperly it can lead to biases and incorrect conclusions [2](Timmons et al, 2015).
Previously, in a survey of 1500 articles containing enrichment analysis, most of these suffered from statistical problems and lack of methodological detail, and we devised general guidelines to combat these issues [3].
The purpose of this study is to assess whether previously published enrichment studies are reliable.

## Aims:

1. To determine whether analysis shown in the selected articles repeatable, 
ie results are internally consistent and no data handling errors were observed.

2. To determine whether methodological issues compromise the reliability of results and the main conclusions.

3. To identify common weaknesses in enrichment studies and come up with practical recommendations to ensure that future analysis is reliable and reproducible.

## Research methods

In our previous study [3] we screened 1500 articles and surveyed their enrichment methods. 
We will further filter this list of articles to those:

* Worked with human gene expression data, as this is the most common application

* Provided the gene profile data as a supplement, to enable re-analysis

* Focus on most used tools EG: DAVID, KOBAS, GSEA

From this list, we will randomly select 20-50 studies and perform the following:

* Test repeatability - we will repeat the analysis as described in the methods section, using tools like DAVID, KOBAS and GSEA.

* Test reliability - we will use the correct methods and see whether the conclusions of the study are still valid.

* Test generalisability - we will repeat the analysis using clusterprofiler and rGSEA in R and see whether the results are consistent.

This analysis will be conducted as much as possible with R/Rstudio using Rmarkdown script.
This will enable workflows to be conducted in an automated and reproducible way.
Critical information like input gene sets, the output data are captured in a HTML report along with the clusterprofiler and rGSEA code and results.

## Expected results and significance

Our previous work identified that methodological problems and lack of detail were extremely common in published articles.
But we do not know whether these articles’ conclusions are invalidated by these problems.
Timmons previously speculated about the validity of two particular studies but did not perform a replication analysis so we cannot be sure.
It is clear that a systematic reproducibility study is required to determine how detrimental these methodological failings are.

From a systematic analysis of 20-50 studies we will identify common weak points in analyses and give practical recommendations to better ensure better reliability in future studies.

## Timeline

Preparation: Dec 2021 - Feb 2022

Begin survey work: Mar - Jun 2022

Analyse results, write paper and thesis: Sept - Oct 2022

## Logistics

Lead investigator has already conducted a pilot study and can share scripts used. It is the student’s responsibility to be up to speed on the background information on enrichment analysis, general R/Rstudio coding and using version control. We may have the opportunity to recruit volunteers or placement students to speed up parts of the work. 

Target Journal: PLoS One?

## Future directions

Depending on the results we may expand the study and request additional help/assistance 
to increase the number of articles or change the scope of the study.

## References

1. Khatri P, Sirota M, Butte AJ. Ten years of pathway analysis: current approaches and outstanding challenges. PLoS Comput Biol. 2012;8(2):e1002375. doi:10.1371/journal.pcbi.1002375

2. Timmons JA, Szkop KJ, Gallagher IJ. Multiple sources of bias confound functional enrichment analysis of global -omics data. Genome Biol. 2015;16(1):186. Published 2015 Sep 7. doi:10.1186/s13059-015-0761-7

3. Wijesooriya K, Jadaan SA, Perera KL, Kaur T, Ziemann M. Guidelines for reliable and reproducible functional enrichment analysis. bioRxiv 2021.09.06.459114; doi: https://doi.org/10.1101/2021.09.06.459114
