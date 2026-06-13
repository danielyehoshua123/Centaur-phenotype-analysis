# Centaur Phenotype Analysis

This repository contains the reproducible R Markdown analysis for:

**The molecular Centaur: Luminal A breast tumors with a lineage-hybrid FOXC1/FOXCUT-high state are associated with stromal/TLS-linked adaptive immune engagement.**

The analysis investigates a FOXCUT/FOXC1-high lineage-hybrid axis in TCGA-BRCA Luminal A breast cancer, including bulk RNA-seq, survival modeling, immune/stromal correlation analysis, xCell2 deconvolution, tumor purity adjustment, and GSE176078 single-cell validation.

## Main files

- `centaur_master_consolidated_final_fixed.Rmd` — executable consolidated analysis.
- `centaur_master_consolidated_final_fixed.html` — knitted output from the Rmd.

## Reproducibility

The Rmd is designed to rebuild or load cached inputs. It can download/rebuild TCGA-BRCA expression, PAM50 metadata, clinical metadata, tumor purity inputs, xCell2 scores when dependencies are available, and GSE176078 Seurat reconstruction when supported processed files are detected.

To run:

```r
rmarkdown::render("centaur_master_consolidated_final_fixed.Rmd")
