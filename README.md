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

## Intermediate Tables
1. **RVIS_Summary.tsv**: RVIS table of variants at each gene.

2. **1000_MSAs.zip** and **Feature_files.zip**: Folders containing 1000 gene MSAs for generations of the species tree.

3. **Genes_1000_combined_4dSites.fastA**: Concatenated multiple sequence alignment containing only 4-fold degenerate sites.
