# **_Temporal proteomic profiling reveals insight into critical developmental processes and temperature-influenced physiological response differences in a bivalve mollusc_**




## Contents

- [Overview](#overview)
- [Repo Contents](#repo-contents)
- [Issues](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/issues)
- [Citation](#citation)

## Overview
**Background:**  Protein expression patterns underlie physiological processes and phenotypic differences including those occurring during early development. The Pacific oyster (_Crassostrea gigas_) undergoes a major phenotypic change in early development from free-swimming larval form to sessile benthic dweller while proliferating in environments with broad temperature ranges. Despite the economic and ecological importance of the species, physiological processes occurring throughout metamorphosis and the impact of temperature on these processes have not yet been mapped out. 

**Results:** Towards this, we comprehensively characterized protein abundance patterns for 7978 proteins throughout metamorphosis in the Pacific oyster at different temperature regimes. We used a multi-statistical approach including principal component analysis, ANOVA-simultaneous component analysis, and hierarchical clustering coupled with functional enrichment analysis to characterize these data. We identified distinct sets of proteins with time-dependent abundances generally not affected by temperature. Over time, adhesion and calcification related proteins acutely decreased, organogenesis and extracellular matrix related proteins gradually decreased, proteins related to signaling showed sinusoidal abundance patterns, and proteins related to metabolic and growth processes gradually increased. Contrastingly, different sets of proteins showed temperature-dependent abundance patterns with proteins related to immune response showing lower abundance and catabolic pro-growth processes showing higher abundance in animals reared at 29°C relative to 23°C. 

**Conclusions:** Although time was a stronger driver than temperature of metamorphic proteome changes, temperature-induced proteome differences led to pro-growth physiology corresponding to larger oyster size at 29°C, and to altered specific metamorphic processes and possible pathogen presence at 23°C. These findings offer high resolution insight into why oysters may experience high mortality rates during this life transition in both field and culture settings. The proteome resource generated by this study provides data-driven guidance for future work on developmental changes in molluscs. Furthermore, the analytical approach taken here provides a foundation for effective shotgun proteomic analyses across a variety of taxa.

## Repo Contents

- ### [Analyses](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses):
	1. [**Proteomics\_Data\_Processing:**](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses/Proteomics_Data_Processing)
		- [Abacus_parameters.txt](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses/Proteomics_Data_Processing/Abacus_parameters.txt):  ABACUS parameter file used in ABACUS analysis of mass spectrometry data
		- [DDA-data-Analyses.md](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses/Proteomics_Data_Processing/DDA-data-Analyses.md):  DDA proteomics analysis workflow that converts files from .raw to .mzXML, searches .mzXML files against C. gigas database, calculates statistics associated with peptide and protein IDs using the Trans Proteomic Pipeline, and correlates protein inferences using ABACUS.  
		- [Pcomet.params.high-low.txt](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses/Proteomics_Data_Processing/Pcomet.params.high-low.txt):  COMET 2016.01 'comet.params.high-low' search parameters used in COMET analysis of mass spectrometry data download from [http://comet-ms.sourceforge.net/parameters/parameters_201601/comet.params.high-low](http://comet-ms.sourceforge.net/parameters/parameters_201601/comet.params.high-low)
		
	2. [**Technical\_Replicates\_PCA:**](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses/Technical_Replicates_PCA)
		- [Technical\_Replicates\_PCA.Rproj](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Technical_Replicates_PCA/Technical_Replicates_PCA.Rproj): R project used to calculate average NSAF values for proteins and run PCA to cluster technical replicates
		- [ClusteringTechnicalReplicates\_and_CalculateAvgNSAFs.R](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Technical_Replicates_PCA/ClusteringTechnicalReplicates_and_CalculateAvgNSAFs.Rmd): R code used to calculate average NSAF values for proteins and run PCA to cluster technical replicates
	
	3. [**PCA\_ASCA\_Functional\_Analysis**](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Analyses/PCA_ASCA_Functional_Analysis):
		- [PCA\_ASCA\_Functional\_Analysis.Rproj](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/PCA_ASCA_Functional_Analysis.Rproj): R project used to run PCA, ASCA, and functional analysis on average protein NSAF values. 
		- [PCA\_ASCA\_Functional\_Analysis.Rmd](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/PCA_ASCA_Functional_Analysis.Rmd): R code used to perform PCA, ASCA, and functional analysis on average protein NSAF values. This produces Figures 2-6, Figures S2-3, and TableS3-6.
		- [Cg\_Giga\_cont\_AA.fa\_BLASTP\_uniprot\_swprot2019.ipynb](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/Cg_Giga_cont_AA.fa_BLASTP_uniprot_swprot2019.ipynb):  Jupyter notebook used to align protein sequences to the Uniprot-KB Swiss-Prot database using BLASTp 
		- [PCA\_model\_summary.txt](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/PCA_model_summary.txt):  PCA results summary
		- [ASCA\_model\_summary.txt](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/ASCA_model_summary.txt):  ASCA results summary
		- [ASCA\_permTest\_summary.txt](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/ASCA_permTest_summary.txt):  Summarized results from ASCA permutation test
		- [TopGO_bkgd.txt](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/TopGO_bkgd.txt): Table of all proteins detected that had associated GO terms that was used for the background term set in TopGO GO enrichment analysis
		- [topGOenrichment_allClades](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/topGOenrichment_allClades.csv): Output of TopGO GO enrichment analysis for all clades
	
	4. [Lit_Compare](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare):
		- [Lit_Compare.Rproj](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare/Lit_Compare.Rproj): R project used to compare proteomics results to published proteomics data.
		- [Lit_Compare.Rmd](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare/Lit_Compare.Rmd): R code used to compare proteomics results to published proteomics data.
		- [Lit_Compare.md](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare/Lit_Compare.md): Markdown file output from knitting R markdown file [Lit_Compare.Rmd](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare/Lit_Compare.Rmd)
		- [Cgiga-uniprot-blastP-out.tab](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare/Cgiga-uniprot-blastP-out.tab): Output from BLASTp of Cg\_Giga\_cont_AA.fa against the species-specific C.gigas reference proteome from the Uniprot database (‘UP000005408\_29159’). Full analysis can be found here: [https://gannet.fish.washington.edu/metacarcinus/Cgigas/BLAST2gigas_uniprot/](https://gannet.fish.washington.edu/metacarcinus/Cgigas/BLAST2gigas_uniprot/)
		- [downloaded\_published\_data](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/Lit_Compare/downloaded_published_data):
			- 2019\_Foulon\_etal\_inSilTRX\_Cgigas.csv is Table 1 from Foulon V, Boudry P, Artigaud S, Guérard F, Hellio C. 2019. In Silico Analysis of Pacific Oyster (Crassostrea gigas) Transcriptome over Developmental Stages Reveals Candidate Genes for Larval Settlement. Int J Mol Sci 20. http://dx.doi.org/10.3390/ijms20010197.
			- gcb13249-sup-0003-tables4.xlsx is Supplementary Table 4 from Dineshram R, Chandramouli K, Ko GWK, Zhang H, Qian P-Y, Ravasi T, Thiyagarajan V. 2016. Quantitative analysis of oyster larval proteome provides new insights into the effects of multiple climate change stressors. Glob Chang Biol 22: 2054–2068. http://dx.doi.org/10.1111/gcb.13249.
			- pr5b00615\_si\_001(table4).pdf is Supplementary Table S4 from Masood M, Raftos DA, Nair SV. 2016. Two Oyster Species That Show Differential Susceptibility to Virus Infection Also Show Differential Proteomic Responses to Generic dsRNA. J Proteome Res 15: 1735–1746. http://dx.doi.org/10.1021/acs.jproteome.5b00615
	
- ### [Data](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Data): 
	1. [ABACUS\_output.tsv](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Data/Abacus_output.tsv):  Output file from ABACUS analysis  
	2. [all_giga-uniprot-blastP-out.nopipe.annotations.tab](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Data/all_giga-uniprot-blastP-out.nopipe.annotations.tab): Proteins mapped to Uniprot database output from [Cg\_Giga\_cont\_AA.fa\_BLASTP\_uniprot\_swprot2019.ipynb](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/Cg_Giga_cont_AA.fa_BLASTP_uniprot_swprot2019.ipynb)
	3. [Average\_adjNSAF\_nozerovals.csv](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Data/Average_adjNSAF_nozerovals.csv):  Average technical replicate NSAF values for each protein with zero values converted to 0.1 (1/8 of the lowest NSAF value). 
	4. [Cg\-Giga\_cont\_AA.fa](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Data/Cg-Giga_cont_AA.fa):  Protein sequence file ('Cg-Giga\_cont\_AA.fa') containing FASTA sequence file of the C. gigas proteome (downloaded from [http://gigaton.sigenae.org](http://gigaton.sigenae.org) as 'contigs.fasta.transdecoder.pep.gz') and common contaminants downloaded from the crapOME (Mellacheruvu et al. Nat Methods 2013). This file is used by proteomics spectral analysis and by UniProt mapping.
	5. [Sample_metadata.csv](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Data/Sample_metadata.csv):  Sample ID and treatment information



- ### [Figures](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Figures):

	1. [Figure 1](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure1.jpg): Pacific oyster developmental proteome during metamorphosis. (A) Diagram depicting life cycle period examined and the collected time points in days post fertilization at each temperature regime. Color bar shows typical timing of metamorphic transitions. The time point when settlement was assessed is denoted by a star. (B) Size distribution based on sorting screen size of oysters at 24 days post-fertilization when settlement was assessed. (C) Number of detected proteins at each time point across two rearing temperatures (23°C, cyan; 29°C, magenta, present in both, purple). 
	2. [Figure 2](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure2.jpg): Temperature most influences 21 and 27 dpf proteomes. (A) Visualization of the first two principal components from principal component analysis separating samples according to their developmental stage and temperature. Samples are labeled by their sampling time point in days post-fertilization (dpf) with color indicating rearing temperature (16°C, brown; 23°C, cyan; 29°C, magenta). (B) Protein abundances (NSAF values autoscaled by row) of proteins most influenced by temperature at 21 and 27 dpf. (C) Summary of biological processes represented by enriched GO terms within each clade for temperature-influenced proteins at 21 and 27 dpf. 

	3. [Figure 3](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure3.jpg): Influence of time on proteomes. (A) Simultaneous component analysis of variation influenced by time, samples are labeled by their sampling time point in days post-fertilization (dpf) with color indicating rearing temperature (23°C, cyan; 29°C, magenta). (B) Protein abundances (NSAF values autoscaled by row) of 217 proteins that contributed the most to time-influenced proteomic variation. (C) Temporal abundance patterns of 217 time-influenced proteins based on 5 clades. Bolded line, autoscaled NSAF clade mean with 95% confidence intervals shown.
	4. [Figure 4](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure4.jpg): Summary of biological processes represented by enriched gene ontology terms within each clade for time-influenced proteins.
	5. [Figure 5](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure5.jpg): Temperature influence on proteomes. (A) Simultaneous component analysis of variation influenced by temperature, samples are labeled by their sampling time point in days post-fertilization (dpf) with color indicating rearing temperature (23°C, cyan; 29°C, magenta). (B) Protein abundances (NSAF values autoscaled by row) of 259 proteins that contributed the most to temperature-influenced proteomic variation. (C) Temporal abundance patterns of 259 temperature-influenced proteins based on 2 clades. Bolded line, autoscaled NSAF clade mean with 95% confidence intervals shown.
	6. [Figure 6](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure6.jpg): Summary of biological processes represented by enriched GO terms within each clade for temperature-influenced proteins. 
	7. [Formatted_Figures.pptx](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Formatted_Figures.pptx): This document contains the journal formatted figures. Powerpoint was used to create panels, add clade color to facetted abundance plots, add summary abundance plots (e.g. [Figure4_colLabs.jpg](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure4_colLabs.jpg) and [Figure6_colLabs.jpg](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure6_colLabs.jpg)) to heatmap columns, and create experimental set-up figure ([Figure 1A](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Figures/Figure1.jpg)).

	All other files in this directory are plots incorporated as figure panels and were directly output from [PCA\_ASCA\_Functional\_Analysis.Rmd](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/Analyses/PCA_ASCA_Functional_Analysis/PCA_ASCA_Functional_Analysis.Rmd). 
	
- ### [Additional_Files:](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/tree/master/Additional_Files)
	1. 	[Additional File 1: Supplemental\_Table\_1.xlsx](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Table_1.xlsx):  Biovolume of oyster seed (mL) settled after 6 days of exposure to high temperatures. Data and plot of oyster counts and size measurements for Figure 1b.
	2. [Additional File 2: Supplemental\_Figures.pdf](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Figures.pdf): PDF of [Supplemental Figure 1](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Figure_1.jpg), [Supplemental Figure 2](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Figure_2.jpg), and [Supplemental Figure 3](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Figure_3.jpg) including figure titles and captions. 

	3. [Additional File 3: Supplemental\_Table\_2.xlsx](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Table_1.xlsx): Preliminary proteome characterization. Data and plot showing overlap between different temperature proteomes at each timepoint underlying Figure 1c.
	4. [Additional File 4: Supplemental\_Table\_3.csv](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Table_3.csv): PCA, hierarchical clustering, and functional analysis results for all detected proteins. 
	5. [Additional File 5: Supplemental\_Table\_4.csv](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Table_4.csv): ASCA time effect analysis, hierarchical clustering, and functional analysis results for all detected proteins. 
	6. [Additional File 6: Supplemental\_Table\_5.csv](https://github.com/shellytrigg/paper-OysterSeed-TimeXTemp/blob/master/SupplementalFiles/Supplemental_Table_5.csv): ASCA temperature effect analysis, hierarchical clustering, and functional analysis results for all detected proteins.

	


## Citation
Trigg, S. A., Mitchell, K. M., Elliott Thompson, R., Eudeline, B., Vadopalas, B., Timmins-Schiffman, E. B., and Roberts, S. B. (2020) Temporal proteomic profiling reveals insight into critical developmental processes and temperature-influenced physiological response differences in a bivalve mollusc. 
