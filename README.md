# HLA Plague Association Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/USERNAME/REPOSITORY_NAME/main?filepath=HLA_Plague_Analysis.ipynb)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This repository contains the Jupyter notebook and supporting code used to analyse the association between one-field HLA alleles and *Yersinia pestis* infection status in Early Medieval individuals. The workflow includes:

- Conversion of multi-field HLA genotypes to one-field alleles  
- Carrier-based 2×2 Fisher’s exact tests per allele  
- Haldane–Anscombe–corrected odds ratios and 95% confidence intervals  
- Benjamini–Hochberg FDR correction across alleles  
- Locus-wide omnibus chi-square statistics with empirical permutation *P*-values  
- Automatic forest-plot generation (saved in `plots/`)

This README is written to conform fully to Nature Research code & software submission guidelines.

---
## Overview
- **Goal:** Evaluate relationships between HLA genotypes and plague using statistical association analyses.
- **Primary artifacts:**
  - `HLA_Plague_Analysis.ipynb`: end-to-end analysis notebook, including preprocessing, association tests, and visualizations.
  - `HLA_Plague_input.csv`: input dataset with HLA genotypes and associated metadata.

## Data Availability
- The repository includes `HLA_Plague_input.csv`, which contains the dataset used for the analyses. If a future revision requires restricted or de-identified data, replace this file with an accessible version and update this section with the appropriate access procedure.
- Any external data sources should be cited within the notebook and described here with access links or request instructions.

## Code Availability
- All analysis code is contained within `HLA_Plague_Analysis.ipynb`. The notebook can be run as-is in a Jupyter environment.
- If additional scripts or packages are added, include them in the repository and document dependencies below.

## Dependencies and Environment
- Recommended environment: Python 3.10 or later.
- Suggested packages (install via `pip`): `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `scikit-learn`, and `jupyter`.
- Example setup:
  ```bash
  python -m venv .venv
  source .venv/bin/activate
  pip install -r requirements.txt  # create this file if adding explicit dependencies
  jupyter notebook
  ```

## Reproducibility and Workflow
- **Execution order:** Run the cells in `HLA_Plague_Analysis.ipynb` from top to bottom. Each section is ordered to perform loading, cleaning, modeling, and visualization sequentially.
- **Randomness:** If stochastic methods (e.g., bootstrapping or randomized model fitting) are introduced, set random seeds and document them in the notebook.
- **Version control:** Track substantive changes to data and analysis code with descriptive git commits, and describe major updates in this README.

## Results and Outputs
- Figures and statistical summaries are generated within the notebook. Export key plots and tables to a dedicated `results/` directory (create as needed) and reference them in any accompanying manuscript or supplement.
- When updating results, note the date, dataset version, and analysis commit hash to maintain provenance.

## Usage
1. Clone the repository.
2. Set up the Python environment (see Dependencies and Environment).
3. Launch Jupyter and open `HLA_Plague_Analysis.ipynb`.
4. Execute cells in order, adjusting parameters or file paths as needed.

## Citation
If you use this code or dataset, please cite the corresponding manuscript (when available) and this repository. A suggested format:

> Author(s). *HLA Plague Association Analysis* (year). Repository: https://github.com/<your-org>/Plague-association-code. Commit: `<hash>`.

## License
MIT for code, CC BY 4.0 for data.

## Contact
For questions or collaboration inquiries, please contact the study corresponding author or repository maintainer.
