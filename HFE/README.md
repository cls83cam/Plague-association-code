# HFE Plague Association Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/USERNAME/REPOSITORY_NAME/main?filepath=HFE%20Analysis.ipynb
)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](
https://doi.org/10.5281/zenodo.XXXXXXX
)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This repository contains the Jupyter notebook and supporting Python code used to analyse the association between HFE variants and *Yersinia pestis* (plague) status in Early Medieval individuals.

The workflow performs:
- parsing and standardisation of HFE genotype fields
- quality-control checks for genotypes and samples
- Association between HFE variants and plague status is evaluated using:
  - 2×2 (or 2×3) contingency tables with Fisher’s exact test and/or chi-square tests, and/or  
  - Logistic regression models with plague status as the outcome and HFE genotype as the predictor, optionally adjusted for covariates (e.g. age, sex, ancestry PCs) if present.
- Effect sizes are reported as odds ratios (OR) with 95% confidence intervals.
- Multiple-testing correction (e.g. Benjamini–Hochberg FDR) is applied if more than one variant/test is evaluated.

Full details are given in the manuscript and Supplementary Methods.

---

## 1. Repository Structure

```
.
├── HFE Analysis.ipynb
├── HFE_input.csv
├── plots/
├── environment.yml
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 2. System Requirements

- Operating systems: Ubuntu 20.04+, macOS 12+, Windows 10/11
- Python: 3.11
- Hardware: 64‑bit computer with ≥8 GB RAM

---

## 3. Software Dependencies

Required Python packages:

- pandas ≥ 2.0
- numpy ≥ 1.26
- scipy ≥ 1.11
- statsmodels ≥ 0.14
- matplotlib ≥ 3.8
- jupyterlab ≥ 4.2

Install via pip:

```
pip install -r requirements.txt
```

Or using conda:

```
conda env create -f environment.yml
conda activate hfe-plague
```

---

## 4. Input Data Specification

Expected columns:

- Sample_ID
- Plague status (case/control)
- HFE variant columns (e.g., C282Y, H63D)

HFE fields contain comma‑separated alleles, e.g.:

```
C282Y, H63D
```

Dataset included:

```
HFE_input.csv
```

---

## 5. Expected Outputs

The notebook writes one or more summary tables to disk, for example:

- `HFE_case_control_summary.csv` – allele/genotype counts and frequencies in cases vs. controls  
- `HFE_association_results.csv` – effect sizes, odds ratios, confidence intervals, raw and adjusted *P*-values  
---

## 6. How to Run

1. Install dependencies.
2. Open the notebook:
```
HFE Analysis.ipynb
```
3. Adjust `INPUT_CSV` if needed.
4. Run all notebook cells in order.

### Runtime:
- Full dataset: <1 minutes

---

## 7. Reproducibility Instructions

To reproduce manuscript results:

```
INPUT_CSV = "HFE_input.csv"
N_PERMS = 5000
```

Run all cells.
Permutation results are reproducible due to fixed seeds.

---

## 8. Code Availability

GitHub:
https://github.com/cls83cam/Plague-association-code

Zenodo archive:
https://doi.org/10.5281/zenodo.XXXXXXX

---

## 9. Data Availability

`HFE_input.csv` is included for analysis.

---

## 10. License

- Code: MIT
- Demo data: CC BY 4.0

---

## 11. Citation

```
Scheib et al. (YEAR)
TO BE PUBLISHED
GitHub: https://github.com/cls83cam/Plague-association-code
DOI:
```

---

## 12. Contact

For questions or reproducibility support, please contact the corresponding author.
