
# 🌍 Life Expectancy Data Analysis – Group 4 Project 2

This project explores global life expectancy data and prepares it for predictive modeling. The dataset includes health, economic, and demographic indicators for various countries across multiple years.

---

## 💡 Hypothesis

> **Health, social, and/or economic factors can be used to model life expectancy outcomes with high predictability.**

This hypothesis guided our modeling choices across both regression and classification tasks. We tested it by examining relationships between key features (e.g., mortality, GDP, schooling, health expenditure) and life expectancy, aiming to build robust predictive models.

---

## 📁 Dataset

- Source: [Life Expectancy Data](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who)
- Records: 2,938
- Features: 22 columns including life expectancy, adult mortality, GDP, education, and immunization coverage.

---

## ✅ Project Progress

### 1. **Data Loading** (`data_cleaning_and_exploration.ipynb`)
- Imported CSV into a pandas DataFrame
- Displayed structural and summary information using `.info()` and `.head()`

### 2. **Data Cleaning**
- Removed leading/trailing spaces in column names
- Dropped rows with missing values in the target column: `Life expectancy`
- Identified and handled missing values in features using visual inspection (histograms)

### 3. **Missing Value Imputation**
- **Used mean** for:
  - `Total expenditure`
  - `Schooling`  
  (both normally distributed)
- **Used median** for all other numeric features with missing values (skewed distributions)

### 4. **Feature Engineering**
- Dropped `Country` due to high cardinality (193 unique values)
- Encoded `Status` (Developing/Developed) using one-hot encoding and replaced the original column

### 5. **Split the Dataset**
- Split the data into training and test data.

### 6. **Feature Scaling**
- Scaled all numeric features (excluding the target) using `StandardScaler`
- Replaced raw numeric values with standardized ones for consistent modeling input

### 7. **Exported Datasets**
- Created CSV files of train and test data, scaled X data, and raw data. 

### 8. **Modeling and Analysis**
#### 🔢 Regression Modeling (`regression_workbook.ipynb`)
- Implemented linear regression and random forest regressor models
- Investigated predictors such as `Adult Mortality` and `infant deaths` using scatter plots and correlation coefficients
- Evaluated model performance using R² and RMSE
- Visualized life expectancy relationships with key numeric predictors

#### 🧠 Classification Exploration (`classification_workbook.ipynb`)
- Introduced classification models to segment life expectancy into categorical bands
- Handled missing values with median imputation
- Used label encoding and feature scaling
- Trained and compared multiple classifiers: Logistic Regression, Random Forest, SVM, KNN, and others
- Evaluated models using accuracy, precision, recall, F1-score, and ROC AUC

### 9. **Created Presentation**
- Presentation created in Google Drive
- Exported Group_4_Project_2_Presentation as PDF and uploaded to repository

---

## 🔧 Requirements

To run the notebooks, install the following packages:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter notebook
```

Or install everything from a requirements file:

```bash
pip install -r requirements.txt
```

Minimum environment:

- Python ≥ 3.8
- Jupyter Notebook
- pandas ≥ 1.3
- scikit-learn ≥ 1.0
- seaborn/matplotlib for visualizations

---

## ✅ Project Summary & Conclusion

Our models confirm that **health, social, and economic indicators** are highly predictive of life expectancy. Both regression and classification approaches supported this:

- Random forest regression achieved an R² over **0.97**, demonstrating excellent predictive power.
- Classification models performed well in segmenting life expectancy into groups, with **Random Forest and SVM** delivering strong scores across multiple metrics.

Thus, our hypothesis is **strongly supported**: accessible public data on economic and health metrics can effectively model life expectancy, with implications for health policy and resource prioritization.

Given **more time**, we could explore feature engineering, interactions between variables, and additional model tuning to further optimize performance, improve both classification and regression accuracy, and potentially expand into other modeling approaches for deeper insights.

---

## 👥 Team Members

- **Chad Bradford**
- **Anshi Mathur**
- **James Segovia**
- **Peyton Lambourne**

---

## 📌 Updated Notes

- The team explored both regression and classification frameworks using the same dataset
- New feature engineering and scaling pipelines were incorporated
- The analysis supports hypothesis testing through statistical correlation and model interpretability
