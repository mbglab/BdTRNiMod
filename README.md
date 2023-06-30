# BdTRNiMod
This repository presents a pipline for characterizing all iModulons of _Bradyrhizobium diazoefficiens_ USDA110. Anand V. Sastry et al. released the procedure for analyzing iModulon (https://github.com/avsastry/modulome-workflow), and we referred to their public code and made some modifications for our research.
## Data
There are four subfolders in the data folder named raw_data, external, processed_data and interim.
The following data files are available in the data folder:

1. raw_data
- log2expset.csv: Gene expression compendium for _Bradyrhizobium diazoefficiens_ USDA110 with log2 transformation.
- metadata_all.csv: Original experimental metadata (e.g. strain descriptions, medium etc.) information.
2. external
- eggNOG_annotations.txt: The eggNOG annotations of _B. diazoefficiens_ USDA110.
- genome.fasta: The genome of _B. diazoefficiens_ USDA110 (GenBank: BA000040.2).
- genome.gff3: The gene annotation of _B. diazoefficiens_ USDA110.
- GO_annotations_curated.csv: The GO annotations of _B. diazoefficiens_ USDA110.
- kegg_mapping.csv: The KEGG annotation of _B. diazoefficiens_ USDA110.
- TRN.csv:  The draft TRN of _B. diazoefficiens_ USDA110 was constructed based on the RegPrecise database and our manually collected data from the literature.
3. processed_data
- A.csv: Condition-specific activities for each iModulon.
- curated_matadata.csv:  Experimental metadata with reference condition and project ID.
- functional_enrichments.csv: Functional annotations on iModulons. 
- gene_info.csv: Descriptive characteristics of genes, including location, operon, and COG group.
- M.csv: Gene coefficients for each iModulon.
4. interim
- bd.json.gz: The IcaData object of _B. diazoefficiens USDA110 _in our research.
- imodulon_table.csv: Detailed information on iModulons. 
## Scripts
We perform the iModulon analysis using the following scripts:

1. 1_expression_QC.ipynb: Quality control of gene expression compendium.
2. 2_optICA: To generate robust independent components for _B. diazoefficiens_ USDA110 gene expression compendium, execute the `run_ica.sh` script in this folder.
3. 3_iModulon_characterization.ipynb: The function of iModulon was analyzed and identified using this script.
4. 4_motif_search.ipynb: Motif enrichment analysis for the promoter region of transcriptional unit.
5. 5_acitve_TRN.ipynb: Active-TRN construction.

All of the above scripts need to be used in the jupyter notebook and loaded with the appropriate environment.
## Requirements:
More about the installation and operation environment requirements, please see https://github.com/avsastry/modulome-workflow and https://github.com/SBRG/pymodulon

## Publication:
Zhi-Peng Gao, Wei-Cheng Gu, Jie Li, Qin-Tian Qiu, Bin-Guang Ma*, Independent component analysis reveals the transcriptional regulatory modules in _Bradyrhizobium diazoefficiens_ USDA110. Forthcoming.
