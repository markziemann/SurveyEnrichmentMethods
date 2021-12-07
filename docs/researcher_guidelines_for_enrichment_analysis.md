# Guidelines for reliable and reproducible functional enrichment analysis

2021-12-07

Kaumadi Wijesooriya, Sameer A Jadaan, Kaushalya L Perera, Tanuveer Kaur, Mark Ziemann

<hr>

Based upon literature and our study called "Urgent need for consistent standards in functional enrichment analysis", 
we have drafted recommended best practice guidelines for conducting functional enrichment analysis.

Links to literature articles are listed at the bottom of this document.

We have broken this list of best practices into two sections, minimum standards and gold standards.
Minimum standards are designed to avoid the most severe methodological issues while requiring minimal effort to address.
These minimum reporting standards will increase the chance that the analysis can be replicated.
Gold standards are aimed towards total transparency, code sharing and long term reproducibility.

## Minimum standards

### Statistics

1. Before starting the analysis, read the tool’s user manual.
Learn what type of statistical test is being conducted and what the null hypothesis is.
Learn whether the test being conducted is a self contained or competitive test and what the advantages/disadvantages are for each test type [1].

2. If making claims about the regulation of a gene set, then results of a statistical test must be shown including measures of significance and effect size.
The number of genes belonging to a pathway on its own is insufficient to infer enrichment [2].

3. Report which statistical test was used.
This will help long term reproducibility, for example if in future the tool is no longer available.
This is especially relevant for tools that report the results of different statistical tests.

4. Always report FDR or q-values (p-values that have been corrected for multiple tests).
This will reduce the chance of false positives when performing many tests simultaneously [2,3].
Report what method was used for p-value adjustment. Bonferroni, FDR and FWER are examples.

5. If ORA is used, it is vital to use a background list consisting of all detected genes, and report this in the methods section [2,4,5].
Avoid tools that don’t accept a background list.

6. If using ORA for gene expression analysis, be sure to conduct ORA tests separately for up- and down-regulated genes.
Combining up- and down-regulated genes into a single list can limit sensitivity [6].

### Reporting

7. Report the origin of the gene sets and the version used or date downloaded.
These databases are regularly upgraded so this is important for reproducibility.

8. Report the tool used and its software version.
As these tools are regularly updated, this will aid reproducibility.
For online tools, record the date the tool was used.

9. Report selection criteria and parameters.
If performing ORA, then the inclusion thresholds need to be mentioned.
If using GSEA or another FCS tool, parameters around ranking, gene weighting and type of test need to be disclosed (eg: permuting sample labels or gene labels). 
Any parameters that vary from the defaults should be reported.

10. Functional enrichment analysis results shouldn’t be considered proof of biological plausibility nor validity of omics data analysis [5].
Such tools are best used to generate new hypotheses; informing subsequent biochemical or signaling experimentation.

## Gold standards

1. Preference FCS and pathway topology tools over ORA tools.
ORA tools are reported to have a lower sensitivity, especially when the number of "significant" genes is low (<100) or high (>3000) [7-9]

2. Include the gene profile data (including any background lists) in the supplementary data to facilitate reproducibility.
TSV or CSV formats are recommended as Excel spreadsheets can be problematic for gene names [10].

3. Scripted analysis workflows are preferred over analysis involving graphical user interfaces because they can attain a higher degree of computational reproducibility [11,12]
Similarly, free and open-source software tools are preferred over proprietary software as it lowers the bar for reproducibility.

4. Foster computational reproducibility by depositing code to a repository like GitHub or Zenodo.
Link the data to the code, so anyone can download and reproduce your results [12].

## Final comments

We drafted these best practices based on our reading of the literature (selected references below),
along with our experience in conducting enrichment analysis and 
examining hundreds of research articles presenting enrichment results.

These are not authoritative, as we are consulting the bioinformatics community for additional input and discussion.
We welcome your contribution; to make a suggestion, please raise an issue to this repository and include any supporing information including links to published articles.

## References

1. Khatri P, Sirota M, Butte AJ. Ten years of pathway analysis: current approaches and outstanding challenges. PLoS Comput Biol. 2012;8(2):e1002375. doi:10.1371/journal.pcbi.1002375

2. Tilford CA, Siemers NO. Gene set enrichment analysis. Methods Mol Biol. 2009;563: 99-121. 

3. Hung JH, Yang TH, Hu Z, Weng Z, DeLisi C. Gene set enrichment analysis: performance evaluation and usage guidelines. Brief Bioinform. 2012;13: 281-291.

4. Tipney H, Hunter L. An introduction to effective use of enrichment analysis software. Hum Genomics. 2010;4: 202-206.

5. Timmons JA, Szkop KJ, Gallagher IJ. Multiple sources of bias confound functional enrichment analysis of global -omics data. Genome Biol. 2015;16: 186.

6. Hong G, Zhang W, Li H, Shen X, Guo Z. Separate enrichment analysis of pathways for up- and downregulated genes. J R Soc Interface. 2014;11: 20130950.

7. Kaspi A, Ziemann M. Mitch: Multi-contrast pathway enrichment for multi-omics and single-cell profiling data. BMC Genomics. 2020;21: 447.

8. Maleki F, Ovens K, Hogan DJ, Kusalik AJ. Gene set analysis: Challenges, opportunities, and future research. Front Genet. 2020;11: 654.

9. Xie C, Jauhari S, Mora A. Popularity and performance of bioinformatics software: the case of gene set analysis. BMC Bioinformatics. 2021;22: 191.

10. Ziemann M, Eren Y, El-Osta A. Gene name errors are widespread in the scientific literature. Genome Biol. 2016;17(1):177.

11. Peng RD. Reproducible research in computational science. Science. 2011;334: 1226-1227.

12. Tan TW, Tong JC, Khan AM, de Silva M, Lim KS, Ranganathan S. Advancing standards for bioinformatics activities: persistence, reproducibility, disambiguation and Minimum Information About a Bioinformatics investigation (MIABi). BMC Genomics. 2010;11: S27.

