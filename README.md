# Cassava Euphorbiaceae Gene Evolution

Welcome to the Cassava Euphorbiaceae Gene Evolution repository! This collection of scripts is designed to facilitate the recreation of analyses, tables, and plots for the study of gene evolutionary selection pressure in Cassava.

## Rmarkdown Workbook
The core of this repository revolves around the Rmarkdown workbook, `CassavaEvolutionarySignalofSelection.Rmd`. This script efficiently executes blocks of code to process dN/dS and other gene metrics, filter genes, perform GO term enrichment, and conduct various analyses.

## Input Files
1. **MSA_DepthList.txt**: Table displaying the number of genomes in the study that comprised the Multiple Sequence Alignments (MSA). MSAs were generated from Cassava V7.1 genes using a dedicated pipeline ([ReelGene Pipeline](https://bitbucket.org/bucklerlab/p_reelgene/src/master/reelGene_pipeline/MSA_models/01_data_preprocessing/)).

2. **LRT_models.txt**: Table of PAML outputs produced using the PAML pipeline ([PAML Pipeline](https://bitbucket.org/bucklerlab/paml_pipeline/src/master/)). It includes Transcript ID, Tree Length computed for the gene tree, F statistics for Cassava vs Euphorbiaceae tree, F statistics for Cassava vs neutral assumptions, dN/dS for the whole gene tree, and dN/dS for the Cassava branch of the gene tree. Multiple sequence alignments containing < 4 assemblies could not be tested.

3. **Assembly_stats.txt**: Basic assembly statistics for assemblies, including estimated genome sizes and coverages for assemblies performed in the study.

4. **CassavaV7.1_Transcripts.stat**: Metrics for Cassava V7.1 gene transcripts, including UTR lengths, CDS length, and start/stop codons.

5. **GO_Groups.tsv**: GO term functions used for GO term enrichment.

6. **MKtest_10pct.tsv**: MK test results with a minor allele frequency of 10% filter.

7. **MeGO_list.txt**: GO terms for Manihot esculenta V7.1 genes (Cassava).

8. **Mesculenta_GOterms_simple.tsv**: Long format of `MeGO_list.txt`.

## Large External Input Files
Large input files can be found through zenodo id: 10.5281/zenodo.10246960 (Upon Publication)
1. 	**CassavaV7_pangenomeDB.txt.gz**: Output table from GENESPACE (https://github.com/jtlovell/GENESPACE) Producing Orthogroups [og].

2. 	**RNA_Processed_Summary.txt.gz**: RNA Expresion for Cassava genes sourced from Cassava study (https://doi.org/10.1038/s41598-021-02794-y).

## Intermediate Tables
1. **RVIS_Summary.tsv**: RVIS table of variants at each gene.

2. **1000_MSAs.zip** and **Feature_files.zip**: Folders containing 1000 gene MSAs for generations of the species tree.

3. **Genes_1000_combined_4dSites.fastA**: Concatenated multiple sequence alignment containing only 4-fold degenerate sites.

## Output Table
**CassavaV8_Gene_Conservation_Analyses.tsv**

Column Names and Explanation

1. Transcript - CassavaV7 gene names + Transcript identifier
2. Total_SNPs - Total Number of SNPs in Cassava Hapmap in the CDS regions of this gene
3. NonSyn_MAF0.01 - Total Number of Nonsynonymoous SNPs in Cassava Hapmap in the CDS regions of this gene with a minor allele frequency filter of 1 %
4. NonSyn_MAF0.05 - Total Number of Nonsynonymoous SNPs in Cassava Hapmap in the CDS regions of this gene with a minor allele frequency filter of 5 %
5. Del_MAF0.01 - Total Number of Deleterious SNPs in Cassava Hapmap in the CDS regions of this gene with a minor allele frequency filter of 1 %
6. Del_MAF0.05  - Total Number of Deleterious SNPs in Cassava Hapmap in the CDS regions of this gene with a minor allele frequency filter of 5 %
7. Nonsyn_Maf1_resid - Residual for regression of NonSyn_MAF0.01 ~ Total_SNPs
8. Nonsyn_Maf5_resid - Residual for regression of NonSyn_MAF0.05 ~ Total_SNPs
9. Del_Maf1_resid - Residual for regression of Del_MAF0.01 ~ Total_SNPs
10. Del_Maf5_resid - Residual for regression of Del_MAF0.05 ~ Total_SNPs
11. og - Orthogolog Group identifier produced by GENESPACE
12. Gene - Gene to which the transcript belongs
13. Chromosome 
14. TL - Tree Length for RAxML tree analyzed by PAML
15. FvsM0 - F-statistic for comparison of Cassava branch of gene tree to rest of the tree
16. FvsNeutral - F-statistic for comparison of Cassava branch of gene tree to a neutral model (dN/dS =1)
17. dNdSTree - dN/dS ratio for the entire gene tree
18. dNdSCassava - dN/dS ratio for Cassava branch of the gene tree
19. Alignment_Depth - # of Species present in Multiple Sequence Alignment used for PAML 
20. UTR5 - Length of 5' Utranslated Region
21. UTR3  - Length of 3' Utranslated Region
22. CDS - Length of Protein Coding Region
23. Start_Codon - 3 base pair start codon
24. Stop_Codon - 3 base pair stop codon
25. pval_m0 - Pvalue from FvsM0 F-statistic
26. pval_neutral - Pvalue from FvsNeutral F-statistic
27. delta_dNdS - (dNdSTree - dNdSCassava)
28. RowNum
29. PnPs - Number of nonsynonymous snps divided by total snps for Cassava HapMap
30. dNdS - Copy of dNdSCassava
31. Alpha_original - MK test stastic 
32. Alpha_Asymptotic - - MK test stastic using asymptotic method (Not Reliable)
33. Alpha_Default - MK test stastic using 5% MAF
34. Mk_test  - MK test stastic using 10% MAF
35. NI - Neutrality Index
36. SigGene - T/F is the gene under significantly relaxed selection (pval_m0 < bonferonni correction)
37. SigGene_inSigOG - T/F is the gene & other genes in Ortholog Group all under significantly relaxed selection (pval_m0 < bonferonni correction)


