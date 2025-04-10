
# RNA-seq PCA / MDS Analysis Pipeline

This repository contains R code for performing Principal Component Analysis (PCA) and Multi-Dimensional Scaling (MDS) plots using gene expression data from lesion-level RNA-seq samples in *Magnaporthe oryzae*–rice interaction experiments.

## Contents
- `mds_analysis.R`: Main R script to process gene expression data, filter, normalize, and plot MDS (PCA-style) clustering.
- `example_data_description.txt`: Description of the data structure expected for analysis.
- (Optional) `data/`: Folder where sample input data or metadata files may be included (e.g., CSV/XLSX with transposed gene counts).

## Requirements
- R version >= 4.0
- Packages:
  - `edgeR`
  - `dplyr`
  - `ggplot2`

Install dependencies in R:
```r
install.packages("BiocManager")
BiocManager::install("edgeR")
install.packages("dplyr")
install.packages("ggplot2")
```

## Overview of Analysis
1. Input a transposed RNA-seq data matrix where rows = samples and columns = genes.
2. Filter out non-fungal samples and known outliers.
3. Generate a gene-by-sample matrix suitable for edgeR.
4. Normalize gene expression.
5. Plot MDS to examine clustering patterns across strain–cultivar–experiment groups.

## How to Run
1. Modify the input path and variable names as needed in `mds_analysis.R`.
2. Run the script in R or RStudio.
3. The output will be a PNG or PDF file showing MDS clustering of samples.

## Citation
Please cite this GitHub repository in any publications or dissertations that use this code. Example:

> RNA-seq PCA/MDS analysis pipeline, [GitHub repository](https://github.com/your-username/RNAseq-PCA-Analysis), accessed Month Year.

---

**Note:** Raw data files are not provided due to size or privacy constraints, but example input structures are described.

For questions, contact: *yourname@yourinstitution.edu*

