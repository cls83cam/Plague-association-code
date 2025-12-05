# HLA Plague Association Analysis

This repository accompanies the study analyzing associations between human leukocyte antigen (HLA) variants and plague outcomes. It is organized to meet Nature Research reporting expectations for reproducibility, transparency, and data availability.

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
Specify licensing terms for the code and data. If unspecified, add an explicit license (e.g., MIT for code, CC BY 4.0 for data) to clarify reuse permissions.

## Contact
For questions or collaboration inquiries, please contact the study corresponding author or repository maintainer.
