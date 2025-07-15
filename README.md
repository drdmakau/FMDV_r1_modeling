# FMDV r1 Modeling: Cross-Neutralization Prediction for Serotype O

This repository contains curated data, analysis scripts, and supplementary materials for the study titled:

**“Machine learning-based prediction of cross-neutralization among FMDV serotype O viruses using VP1 sequence features”**

---

## Repository Structure
The repository is organized as follows:

- `data/` – Raw and processed datasets (e.g., r1 values, GenBank metadata)
- `scripts/` – R scripts for preprocessing, SMOTE, model training, etc.
- `supplementary/` – Supplementary Table 1, additional metadata, GenBank links and suppementary figures
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
| `supplementary/` | `r1_table.csv`              | Final table with virus, serum, r1, GenBank ID, study |
| `scripts/`     | `model_training.R`            | Reproducible R script for full pipeline      |

---

## Modeling Summary

1. Feature Extraction: Derived pairwise amino acid differences at each VP1 site and potential N-glycosylation differences.
2. Class Balancing: Applied SMOTE to oversample minority (“cross-neutralizing”) class in training.
3. Modeling: Trained Random Forest with nested tenfold cross-validation and Boruta feature selection.
4. Validation:
  * Internal: Held-out test sets showed high accuracy, sensitivity, and specificity.
  * External: Independent datasets from UAE, Pakistan, Australia, and Ethiopia confirmed robust performance (minority recall > 0.90).
5. Interpretation: Identified key VP1 residues (48, 100, 135, 150, 151) that drive cross-neutralization predictions.

---

---
Live Demo

A live Shiny dashboard implementing the r1 prediction model can be accessed here:

Shiny App: https://dmakau.shinyapps.io/PredImmune-FMD/

---
## Citation

If you use this repository, please cite the associated manuscript:

> Makau D. N., Arzt J., VanderWaal K., et al. (2025). “Machine learning‑based prediction of cross‑neutralization among FMDV serotype O viruses using VP1 sequence features.” PLOS Computational Biology, (in review)..

---

## 🔗 Links

- **GitHub**: [https://github.com/drdmakau/FMDV_r1_modeling](https://github.com/drdmakau/FMDV_r1_modeling)
- **Zenodo (Archived DOI)**: [TBD]

---

## 📬 Contact

For questions, corrections, or collaborations, contact:  
**Dr. Dennis Makau**  
[University of Tennessee, Knoxville / PEDIL Lab]  
📧 [dmakau@utk.edu](mailto:dmakau@utk.edu)

---
