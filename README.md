# Differential Gene Expression Analysis in Breast Cancer

##  Background
Breast cancer is characterized by widespread dysregulation of gene expression. 
Understanding which genes are altered in cancer versus normal tissue provides 
insights into disease mechanisms and identifies potential therapeutic targets.

##  Research Question
**Which genes are differentially expressed between breast cancer tumor tissue 
and normal breast tissue?**

## Hypothesis
Breast cancer tumors will exhibit significant differential expression compared 
to normal tissue, with:
- Upregulation of cell proliferation and growth-related genes
- Downregulation of tumor suppressor and cell cycle checkpoint genes

##  Objectives
1. Identify significantly differentially expressed genes (DEGs)
2. Quantify expression changes between tumor and normal tissue
3. Visualize expression patterns across samples
4. Interpret findings in biological context

##  Data
- **Source:** The Cancer Genome Atlas (TCGA) Breast Cancer dataset
- **Samples:** 1,100+ tumor samples, 100+ matched normal samples
- **Genes:** 20,530 genes measured via RNA-seq
- **Platform:** Illumina HiSeq RNA-sequencing

##  Methods
- Statistical testing: Student's t-test
- Multiple testing correction: False Discovery Rate (FDR)
- Significance threshold: FDR < 0.05
- Visualization: Volcano plots, heatmaps, box plots

## Key Findings
[You'll fill this in after analysis]
- X genes significantly differentially expressed
- Y genes upregulated in cancer
- Z genes downregulated in cancer
- Notable genes include: [list interesting ones]

##  Biological Interpretation
[You'll fill this in with your biotech expertise]
- Cell cycle genes upregulated (consistent with uncontrolled proliferation)
- Tumor suppressors downregulated (loss of growth control)
- [Other insights from your analysis]

##  Technologies Used
- Python 3.11
- pandas, NumPy (data manipulation)
- SciPy (statistical testing)
- Matplotlib, Seaborn (visualization)
- Jupyter Notebooks (analysis workflow)# 
Differential Gene Expression Analysis in Breast Cancer

##  Project Overview

This project performs comprehensive differential gene expression analysis on breast cancer RNA-seq data from The Cancer Genome Atlas (TCGA). The analysis identifies genes that are significantly dysregulated between tumor and normal breast tissue, providing insights into the molecular mechanisms of breast cancer.
============================================================
KEY FINDINGS 
============================================================

- **15,315 genes** significantly differentially expressed (FDR < 0.05)
- **7,054 genes upregulated** in cancer tissue
- **8,261 genes downregulated** in cancer tissue
- Fold changes ranging from **-7.26 to +6.77 (log2 scale)**

============================================================
ADDITIONAL STATISTICS
============================================================
Total genes analyzed: 20,250
Percentage significant: 75.6%
Tumor samples: 1097
Normal samples: 114

Top 5 Upregulated Genes:
  COL10A1: +6.77
  COL11A1: +5.91
  MMP11: +5.82
  MMP13: +5.79
  CST1: +5.66

Top 5 Downregulated Genes:
  LEP: -7.26
  ADH1B: -6.90
  ADIPOQ: -6.77
  CA4: -6.60
  TUSC5: -6.47


### Top Upregulated Genes (Cancer > Normal)
Key genes with highest expression in tumors include:
- **MMP1, MMP11, MMP13** - Matrix metalloproteinases (ECM remodeling, invasion)
- **NEK2, PKMYT1, KIF4A** - Cell cycle regulation (uncontrolled proliferation)
- **COL10A1, COL11A1** - Collagen genes (structural remodeling)

### Top Downregulated Genes (Cancer < Normal)
Key genes with lowest expression in tumors include:
- **LEP, ADIPOQ, FABP4** - Adipocyte markers (loss of differentiation)
- **PLIN1, CIDEC, CIDEA** - Lipid metabolism (metabolic reprogramming)
- **CA4, TUSC5** - Tumor suppressors (loss of growth control)

##  Biological Interpretation

The analysis reveals classic hallmarks of cancer biology:

1. **Hyperproliferation**: Upregulation of cell cycle genes (NEK2, PKMYT1, UBE2C) indicates uncontrolled cell division
2. **Invasion & Metastasis**: Upregulation of MMP family genes suggests ECM degradation and invasive potential
3. **Dedifferentiation**: Loss of adipocyte markers (LEP, ADIPOQ, FABP4) indicates cancer cells losing normal breast tissue identity
4. **Metabolic Reprogramming**: Downregulation of metabolic genes consistent with the Warburg effect

These findings align with published breast cancer literature and validate our analysis pipeline.

##  Dataset

- **Source**: [The Cancer Genome Atlas (TCGA)](https://www.cancer.gov/tcga) via UCSC Xena
- **Cancer Type**: Breast Invasive Carcinoma (BRCA)
- **Platform**: Illumina HiSeq RNA-sequencing
- **Samples**: 
  - Tumor samples: [~1,100]
  - Normal samples: [~120]
- **Genes**: 20,530 genes measured
- **Data Type**: Log2 normalized gene expression values

##  Methods

### Statistical Analysis
1. **Differential Expression**: Student's t-test for each gene
2. **Multiple Testing Correction**: False Discovery Rate (FDR) using Benjamini-Hochberg method
3. **Significance Threshold**: FDR-adjusted p-value < 0.05
4. **Effect Size**: Log2 fold change calculated as mean(tumor) - mean(normal)

### Visualizations
- **Volcano Plot**: Overview of all genes with fold change vs significance
- **Bar Charts**: Top 20 upregulated and downregulated genes
- **Box Plots**: Detailed comparisons for specific genes of interest

##  Visualizations

### Volcano Plot
![Volcano Plot](results/volcano_plot.png)
*Volcano plot showing 20,530 genes. Red dots indicate significantly upregulated genes in cancer, blue dots indicate significantly downregulated genes.*

### Top Differentially Expressed Genes
![Bar Charts](results/top_genes_barplot.png)
*Bar charts highlighting the top 20 most upregulated (left) and downregulated (right) genes.*

### Gene-Specific Comparisons
![Box Plots](results/boxplots_key_genes.png)
*Box plots comparing expression levels of key genes between tumor and normal tissue.*

## Technologies Used

- **Python 3.11**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **SciPy** - Statistical testing
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical graphics
- **Jupyter Notebook** - Interactive analysis environment


## PROJECT STUCTURE
breast-cancer-rnaseq/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   └── README.md
├── notebooks/
│   └── differential_expression_analysis.ipynb
└── results/
    ├── volcano_plot.png
    ├── top_genes_barplot.png
    ├── boxplots_key_genes.png
    └── differential_expression_results.csv
