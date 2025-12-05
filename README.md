# HLA Plague Association Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/USERNAME/REPOSITORY_NAME/main?filepath=HLA_Plague_Analysis.ipynb
)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](
https://doi.org/10.5281/zenodo.XXXXXXX
)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This repository contains the Jupyter notebook and supporting Python code used to analyse the association between one-field HLA alleles and *Yersinia pestis* (plague) status in Early Medieval individuals.

The workflow performs:
- parsing and standardisation of HLA genotype fields
- conversion to one-field HLA allele resolution
- carrier-based Fisher’s exact tests per allele
- Haldane–Anscombe–corrected odds ratios with 95% confidence intervals
- Benjamini–Hochberg FDR correction
- locus-wide omnibus chi-square statistics with empirical permutation *P*-values
- automated forest-plot generation (saved in the `plots/` folder)

---

## 1. Repository Structure

```
.
├── HLA_Plague_Analysis.ipynb
├── HLA_Plague_input.csv
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
conda activate hla-plague
```

---

## 4. Input Data Specification

Expected columns:

- Sample_ID  
- Plague status (case/control)  
- HLA_A, HLA_B, HLA_C  
- HLA_DRB1, HLA_DQA1, HLA_DQB1, HLA_DPA1, HLA_DPB1  

HLA fields contain comma‑separated alleles, e.g.:

```
HLA_B*07:02, HLA_B*15:01
```

Demo dataset included:

```
demo_data/HLA_Plague_Input_demo.csv
```

---

## 5. Expected Outputs

### Per‑locus association tables:
```
HLA_<locus>_EDI_case_control.csv
```

### Omnibus result summary:
```
HLA_omnibus_summary.csv
```

### Forest plots:
Saved to:
```
plots/<locus>_forest_plot.png
```

---

## 6. How to Run

1. Install dependencies.  
2. Open the notebook:
```
HLA_Plague_Analysis.ipynb
```
3. Adjust `INPUT_CSV` if needed.  
4. Run all notebook cells in order.

### Runtime:
- Demo dataset: <1 minute  
- Full dataset: 3–5 minutes  

---

## 7. Reproducibility Instructions

To reproduce manuscript results:

```
INPUT_CSV = "HLA_Plague_input.csv"
N_PERMS = 5000
```

Run all cells.  
Permutation results are reproducible due to fixed seeds.

---

## 8. Code Availability

GitHub:
https://github.com/USERNAME/REPOSITORY_NAME

Zenodo archive:
https://doi.org/10.5281/zenodo.XXXXXXX

---

## 9. Data Availability

`HLA_Plague_input.csv` is included for analysis.  
For publication with restricted data requirements, substitute an anonymised dataset.

---

## 10. License

- Code: MIT  
- Demo data: CC BY 4.0  

---

## 11. Citation

```
AUTHOR et al. (YEAR)
HLA Plague Association Analysis
GitHub: https://github.com/USERNAME/REPOSITORY_NAME
DOI: https://doi.org/10.5281/zenodo.XXXXXXX
```

---

## 12. Contact

For questions or reproducibility support, please contact the corresponding author.

