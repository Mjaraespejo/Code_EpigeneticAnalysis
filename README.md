# Code_EpigeneticAnalysis
This notebook describes the analysis and interpretation of EM-Seq data generated for developmental timepoints.
EM-seq data was generated from 0-9 hrs, 11-12 hrs and 24-60 hrs embryos, aiming to elucidate the epigenetic dynamics during *Parhyale* embryogenesis

In **3_9 DNA methylation during Parhyale embryogensis.nb.html** are the files and scripts used to analyse EM-seq data from raw reads to data interpretation and visualisaiton. The performed tasks include:
- Quality check of raw methylation reads using using FASTQC (https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
- Reads trimming using *TrimGalore* (https://github.com/FelixKrueger/TrimGalore)
- Reads mapping, deduplication and methylation calling using *Bismark* (https://www.bioinformatics.babraham.ac.uk/projects/bismark/)
- Summarising CpG mapping count, coverage and methylation levels for each stage
- Plot fraction of methylated CpGs per genomic feature including genic, intergenic and TE regions
- Differential methylation analysis using *Methylkit* package (https://bioconductor.org/packages/devel/bioc/vignettes/methylKit/inst/doc/methylKit.html)
- Description of gene-body methyalation patterns
- Definition of threshold to define methylated genes
- Integratation of expression and methylation data to explore potential relationships between expigenetic and transcriptional states
- Estimate statistical differences between developmenatl genes based on  their methylation state.

In **3_10 Impact of DNA methylation loss on Parhyale embryogenesis.nb.html** are the files and scripts used to analyse the impact of DNA methyaltion loss on embryo development. Expression changes weere analysed on embryos treated with the methylation inhibitor 5-aza-2'-deoxycytidine (5-AzadC). The analyses performed include:

- Analysis of embryo surival rates under different conditions
- Expression quantification of 5AZA-treated embryos using FeatureCounts R funciotn (https://www.rdocumentation.org/packages/Rsubread/versions/1.22.2/topics/featureCounts)
- PAC analysis of wild-type and treated embryos
- Differential gene expression (DGE) analysis. Used DESeq2 library to call statistically significant differentially expressed genes, setting were padj < 0.01 and |log10FC| > 1.
- Cluster of expression using genes differentially expressed
- Catgeorisation of genes affected by drug treatment based on developmental categories like matnerla, zygotic and maternal-zygotic.
- Visualisation of results was performed using *pheatmap*, *ggplot* , *ggbreak*, *ggarrange* R packages, among others.
- Gene ontology analysis using *topGO* R package (https://bioconductor.org/packages/release/bioc/html/topGO.html)
  
Please email *alexjapes@gmail.com* if there is any problem, thanks! (Manuel)

[This](https://htmlpreview.github.io/) is a tool to view the html files. 
