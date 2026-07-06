# Research Log

## Session 1
**Date:** 05 July 2026

### Tasks Completed
- Created GitHub repository.
- Created dissertation folder structure.
- Downloaded three approved datasets.
- Loaded the Heart Disease dataset.
- Performed initial data quality assessment.
- Identified missing values.
- Verified duplicate records.
- Generated feature distribution histograms.
- Analysed target class distribution.

### Key Findings
- Dataset contains 303 patient records.
- No duplicate observations.
- Missing values identified only in `ca` and `thal`.
- Original target variable contains five classes with class imbalance.
- Binary target conversion will be performed during preprocessing.

### Challenges
- Loading the dataset due to missing column names.
- Handling missing values represented by '?'.

### Solutions
- Assigned attribute names manually.
- Used `na_values='?'` when importing the dataset.

### Next Session
- Correlation analysis.
- Outlier analysis.
- Missing value visualisation.
- Clinical feature interpretation.
