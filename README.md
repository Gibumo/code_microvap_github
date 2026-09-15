# code_microvap_github

Analysis code for the AJRCCM Research Letter on anatomical compartmentalization
and early temporal dynamics of the respiratory microbiome (NP, ETA, and BAL
samples) in mechanically ventilated ICU patients.

## Contents

`code_micronav_github.Rmd` — unified R Markdown analysis script covering:
alpha/beta diversity, longitudinal and cross-sectional differential abundance
(Wilcoxon, mvabund, MaAsLin2 sensitivity analysis), Random Forest
classification, and figure generation.

## Requirements

R (≥ 4.3.1) with the following packages: `ggplot2`, `ggtext`, `phyloseq`,
`vegan`, `mvabund`, `MaAsLin2`, `caret`, `randomForest`, `pROC`, `rstatix`,
`tableone`, `cowplot`, `patchwork`, `readxl`, `dplyr`.

## Running the script

The script reads raw Mothur output files (`.shared`, `.cons.taxonomy`, and a
metadata `.xlsx`) and writes figures and tables to an output folder.

- **Data location**: set the `DATA_DIR` environment variable to the folder
  containing the raw files, or place them in a `./data` folder alongside the
  script (default).
- **Output location**: set `OUTPUT_DIR`, or results are written to `./output`
  by default (created automatically if it doesn't exist).

Raw patient-level data are not included in this repository.
