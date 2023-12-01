# CassavaEuphorbiaceaeGeneEvolution
Scripts to recreate analyses, tables, and plots for study of gene evolutionary selection pressure in Cassava.  

The bulk of this repository is providing inputs for the Rmarkdown workbook `CassavaEvolutionarySignalofSelection.Rmd`.  This script executes blocks of code to take in dN/dS and oether gene metrics to filter genes, perform GO term enrichment, and other analyses.

# Input Files
`MSA_DepthList.txt` - Table showing the # of genomes in the study that composed the Multiple sequence alignments. Multiple sequence alignments for this proccess were produced from another MSA pipeline using Cassava V7.1 genes as inputs to generate gene MSA from available assemblies (https://bitbucket.org/bucklerlab/p_reelgene/src/master/reelGene_pipeline/MSA_models/01_data_preprocessing/)
`LRT_models.txt` - Table of PAML outputs produced using a pipeline (https://bitbucket.org/bucklerlab/paml_pipeline/src/master/).  Table includes Transcript ID,Tree Length computed for the gene tree,F statistics for Cassava vs Euphorbiaceae tree,F statistics for Cassava vs neurtal assumptions,dN/dS for whole gene tree,dN/dS for the cassava branch of the gene tree.  Multiple sequence alginments containing < 4 assemblies could not be tested.  
`Assembly_stats.txt` - Basic Assembly stats for assemblies, including estiamted genome sizes and coverages for assemblies performed in the study
`CassavaV7.1_Transcipts.stat` - Metrics for Cassava V7.1 gene transcripts including UTR lengths, CDS length, and start/stop codons
`GO_Groups.tsv` - GO term functions used for GO term enrichment
`MKtest_10pct.tsv` - MK test results with a minor allele frequency of 10% filter 
`MeGO_list.txt` - GO terms for Manihot esculenta V7.1 genes (Cassava)
`Mesculenta_GOterms_simple.tsv` - Long Format of `MeGO_list.txt`

# Intermediate Tables
`RVIS_Summary.tsv` - RVIS table of variants at each gene
`1000_MSAs.zip` and `Feature_files.zip` - Folders contain 1000 gene MSAs for generations of species tree
`Genes_1000_combined_4dSites.fastA` - Concatenated Multiple sequence alignment containing only 4-fold degenerate sites
