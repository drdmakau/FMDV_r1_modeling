# FMDV r1 Modeling: Cross-Neutralization Prediction for Serotype O

This repository contains curated data, analysis scripts, and supplementary materials for the study titled:

**“Machine learning-based prediction of cross-neutralization among FMDV serotype O viruses using VP1 sequence features”**

---

## Repository Structure
The repository is organized as follows:

- `data/` – Raw and processed datasets (e.g., r1 values, GenBank metadata)
- `scripts/` – R scripts for preprocessing, SMOTE, PCA, model training, etc.
- `results/` – Outputs including confusion matrices, model metrics
- `figures/` – Manuscript and supplementary figures
- `supplementary/` – Supplementary Table 1, additional metadata, GenBank links
- `README.md` – Project overview (this file)
---

## Project Summary

This project aimed to predict antigenic cross-neutralization (r1 values) between reference vaccine strains and field isolates of FMDV serotype O using machine learning applied to VP1 sequence data. We curated and harmonized 108 serum-virus pairs from 4 published studies spanning 14 countries and multiple topotypes.

---

## Data Sources

- **r1 Values & Metadata**: Extracted from:
  - Tesfaye et al., 2020
  - Yang et al., 2014
  - Upadhyaya et al., 2021
  - Singanallur et al., 2022

- **VP1 Sequences**: GenBank accession numbers are provided in `supplementary/r1_table.csv` and Supplementary Table 1.

---

## Key Files

| Folder         | File                          | Description                                  |
|----------------|-------------------------------|----------------------------------------------|
| `data/`        | `r1_aa_plus_ngly.csv`         | Processed features + outcome used in modeling|
| `data/`        | `serotype.O.csv`              | Original metadata + annotations              |
| `supplementary/` | `r1_table.csv`              | Final table with virus, serum, r1, GenBank ID, study |
| `figures/`     | `PCA_comparison.png`          | PCA visualization of pre-/post-SMOTE data    |
| `scripts/`     | `model_training.R`            | Reproducible R script for full pipeline      |

---

## Modeling Summary

- Feature extraction from VP1 sequences (AA positions, motifs, etc.)
- Class balancing using SMOTE
- Model: Random Forest with nested cross-validation
- External validation confirms improved minority class sensitivity
- PCA confirms synthetic data plausibility post-SMOTE

---

## Citation

If you use this repository, please cite the associated manuscript:

> Makau D., et al. (2025). “Machine learning-based prediction of cross-neutralization among FMDV serotype O viruses using VP1 sequence features.” *[Journal Name]*, (in review).

---

## 🔗 Links

- **GitHub**: [https://github.com/drdmakau/FMDV_r1_modeling](https://github.com/drdmakau/FMDV_r1_modeling)
- **Zenodo (Archived DOI)**: [TBD]

---

## 📬 Contact

For questions, corrections, or collaborations, contact:  
**Dr. Dennis Makau**  
[University of Tennessee, Knoxville / PEDIL Lab]  
📧 `dmakau@utk.edu`

---
