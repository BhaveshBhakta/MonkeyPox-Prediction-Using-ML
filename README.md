## MonkeyPox Prediction

### Project Overview

This project aims to predict the **diagnosis of MonkeyPox** based on various patient-reported symptoms and medical history. By leveraging features such as systemic illness, rectal pain, sore throat, and HIV infection status, the goal is to develop a machine learning model that can assist in the early identification of MonkeyPox cases.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Monkeypox Patients Dataset](https://www.kaggle.com/datasets/muhammad4hmed/monkeypox-patients-dataset)
  * **Size**: 25000 entries (initial), 11 columns. After dropping rows with missing values, the effective dataset size for training is reduced.
  * **Key Features**:
      * Systemic Illness, Rectal Pain, Sore Throat, Penile Oedema, Oral Lesions, Solitary Lesion, Swollen Tonsils, HIV Infection, Sexually Transmitted Infection.
  * **Approach**:
      * Data Cleaning: Dropped 'Patient\_ID' as it's a unique identifier. Rows with missing values (specifically in 'Systemic Illness') were dropped. No duplicates were found.
      * Exploratory Data Analysis: Checked data shape, size, info, descriptive statistics, null values, duplicates, and unique values for each column.
      * Label Encoding: Applied to all categorical and boolean features, and the target variable.
      * Binary Classification: The target variable 'MonkeyPox' is classified as 'Positive' or 'Negative'.
      * Models Used:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 71.5% with Gradient Boosting Classifier.
      * 71.0% with SVC.
      * 71.4% with AdaBoost Classifier.
      * The moderate accuracy scores indicate that distinguishing MonkeyPox based on these symptoms alone can be challenging, and there's room for improvement or the need for more granular data.

-----

### Purpose and Applications

  * Assist healthcare professionals in **preliminary screening for MonkeyPox**, especially in resource-limited settings.
  * Support rapid identification of potential cases to facilitate early isolation and contact tracing.
  * Aid in public health surveillance by predicting geographical areas or populations at higher risk.
  * Contribute to understanding the symptomatic profile of MonkeyPox for better diagnostic tools.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/MonkeyPox-Prediction-Using-ML.git
cd MonkeyPox-Prediction-Using-M
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Improving model performance through advanced hyperparameter tuning and exploring different model architectures.
  * Investigating more sophisticated methods for handling missing values in 'Systemic Illness' instead of dropping rows.
  * Considering the use of more granular or time-series symptom data if available.
  * Adding explainability (e.g., SHAP or LIME) to understand which symptoms are the strongest predictors of MonkeyPox.
