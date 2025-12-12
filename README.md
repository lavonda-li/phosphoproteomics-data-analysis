# Phosphoproteomics Data Analysis

Replication of the phosphoproteomics analysis from:

> **"In-depth phosphoproteomic profiling of the insulin signaling response in heart tissue and cardiomyocytes unveils canonical and specialized regulation"**
> Achter et al., 2024 ([PMC11264841](https://pmc.ncbi.nlm.nih.gov/articles/PMC11264841/))

## Overview

This project demonstrates how AI agents can assist medical researchers with limited formal bioinformatics training to conduct hands-on, reproducible data analyses. The analysis replicates the core phosphoproteomics workflow from the paper.

## Data

- `Normalised_phosphopeptide_quantities_Bulk.txt` - Main dataset with 10,400 phosphopeptides across 11 samples
- `12933_2024_2338_MOESM*.xlsx` - Supplementary data files from the paper

## Analysis

The Jupyter notebook `phosphoproteomics_analysis.ipynb` covers:

1. **Data Loading & Exploration** - Import and inspect phosphopeptide data
2. **Quality Control** - Sample correlation analysis and PCA
3. **Differential Analysis** - Compare insulin vs control groups with t-tests and FDR correction
4. **Visualization** - Volcano plots and heatmaps
5. **Biological Validation** - Check known insulin signaling pathway markers

## Setup

```bash
# Install dependencies with uv
uv sync

# Run Jupyter notebook
uv run jupyter notebook phosphoproteomics_analysis.ipynb
```

## Key Findings

The paper identified **84 insulin-regulated phosphorylation events** (73 upregulated, 11 downregulated) using:
- |log2 fold change| > 0.3
- Benjamini-Hochberg adjusted p-value < 0.1

## License

This is an educational project for learning purposes.
