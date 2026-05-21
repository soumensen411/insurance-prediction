# 🏥 Insurance Charges Prediction
## Overview

Insurance companies need to accurately estimate medical costs for their customers. This project builds a regression model to **predict insurance charges** using features like age, sex, BMI, number of children, smoking habit, and residential region.

The goal is to understand which factors most influence insurance premiums and build a model that can generalize well to new data.

---

## Dataset

**File:** `insurance.csv`  
**Rows:** 1,338 | **Columns:** 7

| Column | Type | Description |
|--------|------|-------------|
| `age` | int | Age of the primary beneficiary |
| `sex` | object | Gender of the beneficiary (`male` / `female`) |
| `bmi` | float | Body Mass Index |
| `children` | int | Number of children/dependents covered |
| `smoker` | object | Whether the person smokes (`yes` / `no`) |
| `region` | object | Residential region in the US (`northeast`, `northwest`, `southeast`, `southwest`) |
| `charges` | float | Individual medical costs billed by insurance (**target variable**) |

---

## Project Structure

```
Insurance-Prediction/
│
├── insurance.csv                  # Dataset
├── insurance_prediction.ipynb     # Main Jupyter Notebook
└── README.md                      # Project documentation
```

---

## Tech Stack

- **Language:** Python 3
- **Environment:** Jupyter Notebook
- **Libraries:**
  - `pandas` – data manipulation
  - `numpy` – numerical operations
  - `matplotlib` / `seaborn` – data visualization
  - `scikit-learn` – model building and evaluation

---

## Workflow

The notebook follows a standard ML pipeline:

1. **Data Loading** – Load `insurance.csv` using pandas
2. **Exploratory Data Analysis (EDA)**
   - Distribution of charges
   - Correlation heatmap
   - Boxplots and scatter plots for key features
3. **Data Preprocessing**
   - Encoding categorical variables (`sex`, `smoker`, `region`)
   - Feature scaling if required
4. **Model Building**
   - Linear Regression
   - (Additional models if explored: Ridge, Random Forest, etc.)
5. **Model Evaluation**
   - R² Score
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE) / Root MSE
---

## Results

> Key findings from the analysis:

- **Smoking** is the strongest predictor of high insurance charges.
- **Age** and **BMI** also show significant positive correlation with charges.
- The model achieved a satisfactory R² score on the test set, demonstrating reasonable predictive power.

---
