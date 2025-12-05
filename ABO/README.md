
# ABO Plague Association Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/USERNAME/REPOSITORY_NAME/main?filepath=HFE%20Analysis.ipynb
)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](
https://doi.org/10.5281/zenodo.XXXXXXX
)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This repository contains the Jupyter notebook and supporting Python code used to analyse the associations between blood-group–related genetic variants and Yersinia pestis (plague) case–control status in Early Medieval individuals. It implements a reproducible workflow suitable for peer review and public release.

The analysis includes:

1. Loading blood-group genotype data and plague phenotype labels.
2. Computing allele and genotype frequencies in cases and controls.
3. Performing association tests (e.g., Fisher’s exact tests or logistic regression).
4. Estimating effect sizes, odds ratios, and confidence intervals.
5. Applying multiple-testing correction where applicable.

Full details are given in the manuscript and Supplementary Methods.

---

## 1. Repository Structure

```
.
├── BloodGroup_Analysis.ipynb
├── BloodGroup_input.csv
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
conda activate abo-plague
```

---

## 4. Input Data Specification

A CSV file containing:

- `Sample_ID` – unique identifier per individual  
- A case–control indicator (e.g. `Plague_status` with values `"case"` / `"control"` or equivalent)  
- Blood-group variant columns, for example:  
  - `O`  
  - `A`
  - `AB`

The default path to the input file is set in a configuration cell (e.g. `INPUT_CSV = "BloodGroup_input.csv"`); this can be modified by the user as needed.

---

## 5. Expected Outputs

The notebook produces:

- `BloodGroup_O_stats_summary.csv` – effect sizes, odds ratios, confidence intervals, raw and adjusted *P*-values  
   
---

## 6. How to Run

1. Install dependencies.
2. Open the notebook:
```
BloodGroup_Analysis.ipynb
```
3. Adjust `INPUT_CSV` if needed.
4. Run all notebook cells in order.

### Runtime:
- Full dataset: <1 minutes

---

## 7. Reproducibility Instructions

To reproduce manuscript results:

```
INPUT_CSV = "BloodGroup_input.csv"
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

`BloodGroup_input.csv` is included for analysis.

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
