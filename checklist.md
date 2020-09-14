# Best practices list for functional enrichment analysis

The goal is to avoid the common pitfalls in pathway analysis, and ensure reproducibility.

## Nomenclature

Definitions are important:

* Functional enrichment analysis (FEA)

* Overrepresentation analysis (ORA)

* Functional class scoring (FCS)

* Gene set library

* Pathway topology

* Foreground set

* Background set

* False discovery rate correction

* Reproducibility/replicability

## Reporting standards
 
For reproducibility, there are a number of items that need to be reported in the methods section:

* Clear description of how the gene profiling data were processed.

* What gene set library/libraries were used?

* What version of gene set library was used or what was the date they were acquired?

* What tool was used?

* What version of the tool was used? If there is no version number, for example a web app, what was the date the app was used?

* What parameters were used? If non-default parameters were used, note the reason.

* What statistical test was used? This is particularly important for tools that report results of multiple tests.

* What is the threshold for significance?

* What type of p-value adjustment for multiple testing was used?

* If using ORA, what background list was used?

* If using FCS, what is the ranking/scoring algorithm used?

In the results section:

* If particular gene sets are mentioned, it is important to provide data on their statistical significance as well as the degree of enrichment.

* If multiple analyses are performed with different gene set libraries and analytical tools, it is important to state in the results or fgure legend which tool/database were used to generate the data.

* Report adjusted p-values.

## Background list

The choice of background list is a major decision that changes the hypothesis being tested. 
Tools that do not allow a user to provide a background list should not be used at all.

## Correcting for multiple tests

Choose a method like FDR, Bonferonni, Yeukateli for adjusting for multiple tests.
If testing multiple gene set libraries then it is a good idea to adjust for all gene sets.

## Perform a test

Sometimes it is good to know the proportions of genes belonging to each function but this doesn't tell us much about difference to the null.
This is why a statistical test of enrichment is required.

## Combining up and downregulated genes

It is common that researchers merge these lists but there isn't much scientific basis for it.

## Small RNA analysis

A common analysis of miRNA-seq results in in a list of one or more DE miRs. 
The targets are mined from Diana miRpath or similar and enrichment analysis can be performed but the background used is rarely appropriate for the test.

## Epigenetics analysis

Unlike gene expression analysis, epigenetics has some particular problems.

* More than one location can regulate a gene, and genes have different sizes which causes a bias.

* A particular genomic region may be assigned to more than one gene.

## Additional tips to boost reproducubility

* Preferably use well supported tools eg: packages in CRAN, BioC, standalone software in repositories rather than individual webages, due to potential link-rot. 
(consider the 10 year test)

* To that end, non-propriety open access software is more readily reproducible and the underlying code verifiable.

* If using a programming language - sharing analysis code can assist with reproducibility but it is not a panacea.

* If the profiling data are not easily obtained from public databases then include the input data to the functional enrichment analysis as a supplemental file.

## Conclusions

Most of the problems described here stem from improper use of ORA tools, likely because these are easy to use and quickly generate outputs.
In contrast FCS based tools were rarely misused in a way that violated assumptions.
It is also noted that ORA based methods have poorer performance as compared to FCS methods.
Therefore FCS methods are in general preferable to ORA.
A common application of ORA is in the interpretation of intersected gene lists, from for example multiple treatment groups or omics analyses.
Even in these cases, multivariate FCS tools have been devised and are likely superior to intersecting lists of genes followed by ORA.
In conclusion, there is a need to educate researchers and reviewers so these major pitfalls of enrichment analysis can be avoided.
