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

## Session 2 – 6 July 2026

### Tasks completed
- Loaded the Cleveland Heart Disease dataset.
- Performed exploratory data analysis (EDA).
- Examined feature distributions and missing values.
- Generated correlation heatmap and boxplots.
- Saved all visualisations to the Figures folder.
- Successfully configured Git and synchronized the project with GitHub.

### Outcome
The dataset structure and quality are now understood. The project repository is fully configured, and the data is ready for preprocessing.
# Research Log

## 06 July 2026 – Notebook 02: Data Preprocessing

### Activities Completed
- Loaded the Cleveland Heart Disease dataset from the UCI repository.
- Verified dataset structure and dimensions (303 observations, 14 variables).
- Investigated missing values and identified missing data in the `ca` and `thal` features.
- Applied most-frequent-value imputation to handle missing values while preserving sample size.
- Converted the original multi-class target variable into a binary classification target:
  - 0 = No heart disease
  - 1 = Presence of heart disease
- Evaluated class distribution and confirmed that the dataset is relatively balanced (54.1% vs 45.9%).
- Split the dataset into training and testing sets using stratified sampling (80/20 split).
- Applied feature standardisation using StandardScaler.
- Saved processed datasets for future modelling stages.
- Saved the fitted scaler to support reproducibility.

### Key Findings
- Missing values were limited to two variables (`ca` and `thal`) and were successfully imputed.
- No duplicate records were identified.
- The dataset does not require SMOTE due to acceptable class balance.
- Data preprocessing pipeline is now complete for the Heart Disease dataset.

### Challenges Encountered
- Initial file path issues occurred due to dataset folder structure.
- Resolved path configuration using a modular dataset-loading approach.

### Next Steps
- Train baseline machine learning models:
  - Logistic Regression
  - Random Forest
  - XGBoost
- Evaluate models using Accuracy, Precision, Recall, F1-score and ROC-AUC.


Session 3 (Classical Machine Learning Models)

## 06 July 2026 – Notebook 02: Classical Machine Learning Models

Duration: (4.5 hours)

Objectives
Develop baseline machine learning models for heart disease prediction.
Compare multiple classical algorithms using a consistent evaluation framework.
Tasks Completed
Implemented Logistic Regression.
Implemented Random Forest.
Implemented XGBoost.
Evaluated all models using:
Accuracy
Precision
Recall
F1-score
ROC-AUC
Confusion Matrix
ROC Curve
5-fold Cross-Validation
Saved trained models using Joblib.
Generated and exported the model comparison table (classical_ml_results.csv).
Committed all work to Git and pushed changes to GitHub.
Key Findings
Random Forest achieved the highest overall predictive performance on the Cleveland Heart Disease dataset.
Logistic Regression provided a strong and interpretable baseline.
XGBoost performed competitively but did not outperform Random Forest on this dataset.
Reflection

The experiments demonstrated the importance of comparing multiple algorithms rather than assuming that more complex models automatically achieve superior performance. The results provide a strong baseline for comparison with the Deep Neural Network in the next phase of the project.

### Next session
- Create preprocessing pipeline.
- Handle missing values.
- Convert target variable to binary.
- Save processed dataset.

## Session 4 – Classical Machine Learning Models

**Date:** 07 July 2026

**Duration:** 4–5 hours

### Objectives
- Implement and compare classical machine learning models for heart disease prediction.

### Activities Completed
- Developed a Logistic Regression classifier.
- Developed a Random Forest classifier.
- Developed an XGBoost classifier.
- Evaluated all models using Accuracy, Precision, Recall, F1-score and ROC-AUC.
- Generated Confusion Matrices and ROC Curves.
- Performed 5-fold Cross-Validation.
- Saved trained models using Joblib.
- Created and exported a comparison table (`classical_ml_results.csv`).
- Committed Notebook 03 work to Git.

### Key Findings
- Random Forest achieved the highest predictive performance.
- Logistic Regression provided a strong baseline.
- XGBoost performed competitively but did not outperform Random Forest.

### Reflection
Notebook 03 established a complete baseline comparison of classical machine learning algorithms. These results will serve as the benchmark for evaluating the Deep Neural Network model in the next phase of the dissertation.

