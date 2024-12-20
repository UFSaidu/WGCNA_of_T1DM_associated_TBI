# WGCNA_of_T1DM_associated_TBI

## Introduction
Diabetes (T1DM) can coexist with Traumatic brain injury (TBI) and recent studies have indicated that T1DM exacerbates the outcomes of TBI, leading to more severe cognitive deficits and increased risk of complications. This study sought to identify key genes and investigate the underlying molecular mechanisms and potential therapeutic targets for T1DM-associated TBI.

## Methodology
Four microarray datasets related to T1DM and TBI downloaded from GEO repository were used in this study. The datasets were normalized, filtered, and batch corrected using TMM-normalization method in "edgeR" package and "ComBat" function in "sva" package. The processed data were analyzed using "Limma" bioconductor package to screen for differentially expressed genes (DEGs). Using whole expression data, WGCNA analysis was performed to identify significant genes in disease-related modules using hierarchical clustering of genes and "Spearman correlation". GSEA and Metascape was used to identify enriched biological processes of DEGs. "GO" and "KEGG" analysis using "clusterProfiler" were used for functional enrichment annotation of the module genes. Protein Network analysis was constructed using "STRING" and the network was exported into "Cytoscape". Next, the "cytoHubba" plugin was used for hub genes identification. Genes that were significantly associated with both T1DM and TBI were identified based on the overlap of TIDM-related module genes and TBI-related module genes. Finally, the identified shared genes were functionally annotated using "GO" and "Reactome" to further understand their biological functions in T1DM-associated TBI.

## Results
### Identification and GSEA analysis of DEGs
Using Limma, a total of 284 DEGs were identified in T1DM, of which 11 were upregulated and 9 were downregulated. GSEA and Metascape analysis showed that T1DM DEGs were significantly enriched in "lipid metabolic process and response to xenobiotic stimulus". A total of 584 DEGs were identified in TBI, of which 186 were upregulated and 9 were downregulated. GSEA and Metascape analysis showed that the TBI DEGs were mainly enriched in "immune response-regulating signaling pathways". 

### WGCNA identification of disease-related significant genes
Using WGCNA, 122 genes were identified in T1DM-related significant modules, and 368 genes were identified in TBI-related significant modules. GO and KEGG analysis showed that T1DM-related module genes were correlated with "lipid metabolic process and stress response", and the TBI-related module genes were correlated with "innate and adaptive immune response". 

### Identification of hub genes
A PPI network analysis identified 20 hub genes (Rpl23, Rps3a, Hmgcs2, Rps6, Rpl5, Rpl17, Rps24, Rpl23a, Rps4x, Mtor, Pdk4, Rpl9, Rps15a14, Rpl30, Rpl31, Rps25, Rps27a-2, Kcna4, Slc2a4, and Cpt1a) from T1DM-related module genes. The hub genes were primarily related to "Ribosome biogenesis and RNA post-transcriptional regulation". A PPI network analysis identified 20 hub genes (Ptprc, Tp53, Stat1, Stat3, Tyrobp, Itgad, Csf1r, Itgb2, Rac2, Icam1, Myd88, Cd44, Vav1, Aif1, C1qa, Laptm5, B2m, Fcer1g, and Lyn) from TBI-related module genes. The hub genes were primarily related to "inflammatory mediators and immune response". 

### Finding commmon genes of diabetes-associated TBI
Based on the overlap of T1DM-related module genes and TBI-related module genes, Cmklr1, Mgst1, and Plin2 were identified as key genes of T1DM-associated TBI. Functional enrichment annotation using GO showed that the shared genes were primarily enriched in cellular response to lipid hydroperoxide, cytokine mediated receptor signaling activity, regulation of sequestering of triglyceride, negative regulation of IL-12 production, positive regulation of lipid storage, and positive regulation of macrophage chemotaxis. Furthermore, Reactome showed that Cmklr1 , Mgst1, and Plin2 were primarily related to inflammation, neutrophil degranulation, and lipid storage, respectively. 

## Conclusion
We identified key genes and investigated the enriched biological processes in diabetes-associated TBI. We found that genes associated with ribosome biogenesis and lipid metabolic process were implicated in type 1 diabetes. Similarly, we found that immune-related genes were significantly upregulated in TBI which highlighted the significant role of inflammation in TBI pathology. Further, Cmklr1, Mgst1 and Plin2 were the common genes associated with both diabetes and TBI, and are related to inflammation and lipid storage. Thus, we concluded that dysregulation of lipid sequesteration and neuroinflammation are the potential molecular mechanisms of diabetes-associated TBI. Cmklr1, Mgst1, and Plin2 may be important biomarkers and potential treatment targets for diabetic TBI. Hence, the specific role of Cmklr1, Mgst1, and Plin2 in diabetes, TBI, and in diabetes-associated TBI, and in-vivo experimental validations should be the fucus of future investigations.

### Publication
 [Preprint on biorXiv] (https://doi.org/10.1101/2024.10.12.615673)
