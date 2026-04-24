# 🔫 NYPD Shooting Fatality Classification

Predicting whether a shooting incident results in a fatality using machine learning — applied to real NYPD historical data.

---

## 📌 Project Overview

This project builds a binary classification model to predict the fatality outcome (`STATISTICAL_MURDER_FLAG`) of shooting incidents in New York City. The dataset is sourced from the [NYPD Shooting Incident Data (Historic)](https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8) — a public record of every shooting incident reported in NYC.

---

## 🎯 Objective

Given features like borough, time of day, victim/perpetrator demographics, and location — can we predict whether a shooting will be fatal?

---

## 🗂️ Project Structure

```
├── NYPD_Shooting_Fatality_Classification.ipynb   # Main notebook
├── NYPD_Shooting_Fatality_Classification.pptx    # Project presentation
└── nypd_fatality_classifier.pkl                  # Saved best model
```

---

## 🔧 Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, imbalanced-learn (SMOTE), SHAP, Matplotlib, Seaborn

---

## 📊 Workflow

1. **Exploratory Data Analysis** — Distribution of fatalities, borough-level analysis, temporal trends, demographic breakdowns
2. **Data Preprocessing** — Handling nulls, encoding categoricals, feature engineering (time of day, weekend flag, etc.)
3. **Class Imbalance Handling** — Applied SMOTE on the training set to address the imbalanced target variable
4. **Model Comparison** — Trained and evaluated 6 models:
   - Logistic Regression
   - Decision Tree
   - K-Nearest Neighbors
   - Random Forest
   - Gradient Boosting
   - XGBoost ✅ *(best performer)*
5. **Hyperparameter Tuning** — GridSearchCV on XGBoost
6. **Model Interpretability** — SHAP summary plots to explain feature contributions
7. **Model Export** — Saved final model as `.pkl` for deployment

---

## 📈 Results

| Metric | Score |
|--------|-------|
| Model | Tuned XGBoost |
| Evaluation | Accuracy, Precision, Recall, F1, ROC-AUC |
| Interpretability | SHAP feature importance |

> Full metrics available in the notebook output.

---

## 💡 Key Insights

- Fatality rates vary significantly across NYC boroughs
- Time of day and victim age group are among the strongest predictors
- SHAP analysis reveals which features drive individual predictions

---

## 🚀 How to Run

1. Download the dataset from the [NYC Open Data portal](https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8) as `.xlsx`
2. Open the notebook in Google Colab
3. Upload the `.xlsx` file when prompted
4. Run all cells in order

---

## 👩‍💻 Author

**Eva Shukla** — Data Science & Machine Learning  
[LinkedIn](https://www.linkedin.com/in/evashukla) 
