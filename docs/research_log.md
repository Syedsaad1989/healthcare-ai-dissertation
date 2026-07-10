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

## Session 4 – Deep Learning Model

**Date:** 08 July 2026

### Objectives
- Develop a Deep Neural Network for heart disease prediction.
- Compare its performance with classical machine learning models.

### Activities Completed
- Loaded the preprocessed training and testing datasets.
- Built a Deep Neural Network using TensorFlow/Keras.
- Applied dropout regularisation and early stopping.
- Trained the model using the training dataset.
- Evaluated performance using Accuracy, Precision, Recall, F1-score and ROC-AUC.
- Generated learning curves, confusion matrix and ROC curve.
- Saved the trained model (`deep_learning_model.keras`).
- Created an updated comparison table including all four models.

### Results
- Accuracy: 0.8525
- Precision: 0.8276
- Recall: 0.8571
- F1-score: 0.8421
- ROC-AUC: 0.9524

### Key Findings
- The Deep Learning model achieved strong predictive performance.
- Random Forest remained the best-performing model overall.
- The findings indicate that classical ensemble methods can outperform deep learning on small structured tabular datasets.

### Next Session
- Perform SHAP explainability analysis for the best-performing model (Random Forest).

## Session 5 – SHAP Explainability Analysis

**Date:** 09 July 2026

### Objectives
- Interpret the best-performing Random Forest model using SHAP.
- Identify the most influential clinical features affecting heart disease prediction.

### Activities Completed
- Loaded the trained Random Forest model.
- Applied SHAP (SHapley Additive Explanations).
- Generated a global feature importance bar plot.
- Generated a SHAP summary (beeswarm) plot.
- Generated a SHAP waterfall plot for an individual prediction.
- Saved all explainability visualisations.

### Key Findings
- SHAP successfully explained both global and local model behaviour.
- The analysis identified the clinical variables with the greatest influence on heart disease prediction.
- Explainability improves the transparency and trustworthiness of the machine learning model for healthcare applications.

### Reflection
The SHAP analysis demonstrated that high predictive accuracy alone is insufficient in healthcare. Providing explanations for individual predictions enhances model transparency and supports responsible use of AI in clinical decision-making.

### Next Session
- Prepare final model evaluation and dissertation-ready visualisations.
- Summarise results from all machine learning and deep learning models.

## Session 6 – Final Model Evaluation

**Date:** 07 July 2026

### Objectives
- Compare all developed machine learning and deep learning models.
- Identify the best-performing classifier.
- Produce dissertation-ready figures and summary tables.

### Activities Completed
- Loaded the consolidated model comparison results.
- Compared Logistic Regression, Random Forest, XGBoost and Deep Learning models.
- Created accuracy comparison and overall performance comparison charts.
- Identified the best-performing model based on evaluation metrics.
- Exported the final results table for inclusion in the dissertation.

### Key Findings
- Random Forest achieved the highest overall predictive performance.
- Deep Learning achieved competitive ROC-AUC performance but did not outperform Random Forest.
- Classical ensemble learning methods proved highly effective for this structured clinical dataset.

### Reflection
The final evaluation confirmed that Random Forest is the most suitable model for heart disease prediction in this study. Combining predictive performance with SHAP explainability provides a transparent and reliable AI solution for healthcare applications.

### Project Status
- Notebook 01 – Exploratory Data Analysis ✓
- Notebook 02 – Data Preprocessing ✓
- Notebook 03 – Classical Machine Learning ✓
- Notebook 04 – Deep Learning ✓
- Notebook 05 – SHAP Explainability ✓
- Notebook 06 – Final Model Evaluation ✓

### Next Phase

## Session 7 – Diabetes Dataset Exploratory Data Analysis

**Date:** 10 July 2026

### Objectives
- Explore the structure and characteristics of the Pima Indians Diabetes dataset.
- Identify data quality issues.
- Assess class distribution and feature relationships.
- Prepare the dataset for preprocessing and model development.

### Activities Completed
- Loaded the Pima Indians Diabetes dataset.
- Examined dataset dimensions and feature information.
- Investigated zero-valued clinical measurements representing missing data.
- Confirmed there were no duplicate records.
- Analysed the target class distribution.
- Generated feature histograms, correlation heatmap, and boxplots.
- Saved all visualisations to the Figures directory.

### Key Findings
- The dataset contains 768 patient records and 9 variables.
- Zero values were identified in Glucose, Blood Pressure, Skin Thickness, Insulin, and BMI, indicating missing clinical measurements.
- The dataset contains no duplicate observations.
- The target variable shows a moderate class imbalance (65.1% non-diabetic, 34.9% diabetic).
- Glucose, BMI, and Age demonstrate notable relationships with diabetes outcome.

### Next Steps
- Perform data preprocessing.
- Impute missing clinical measurements.
- Apply feature scaling.
- Train and evaluate Logistic Regression, Random Forest, XGBoost, and Deep Learning models.
- Interpret predictions using SHAP explainability.

