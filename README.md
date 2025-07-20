# Credit Score Classification Project

This project focuses on building a machine learning model to classify credit scores based on various financial and demographic attributes. The dataset contains customer credit-related features, and the goal is to classify the `Credit_Score` into categories such as **Poor**, **Standard**, and **Good**.

## 📁 Dataset Overview

The dataset used contains various customer-related information such as:
- Age
- Occupation
- Annual Income
- Number of Loans
- Number of Delayed Payments
- Credit Mix
- Outstanding Debt
- Changed Credit Limit
- Payment Behaviour
- And many more...

The target variable is `Credit_Score`, which has been encoded as:
- `0` = Poor
- `1` = Standard
- `2` = Good

## 🧹 Data Preprocessing Steps

1. **Removed Irrelevant Columns**: Dropped `ID`, `Customer_ID`, `Name`, `SSN`, `Type_of_Loan`, and `Credit_History_Age`.
2. **Handled Missing and Corrupt Values**:
   - Replaced placeholders like `_`, `_______`, and `!@9#%8` with `NaN`.
   - Imputed missing values using forward-fill and back-fill strategies.
3. **Data Cleaning**:
   - Converted appropriate columns to numeric types.
   - Cleaned and encoded categorical features.
4. **Outlier Removal**:
   - Used IQR method to remove outliers from the `Age` column.
5. **Feature Encoding**:
   - Used `LabelEncoder` to encode categorical variables.

## 📊 Exploratory Data Analysis (EDA)

- Visualized the distribution of the `Age` column using boxplots before and after removing outliers.

## 📈 Feature Engineering

- Encoded `Payment_of_Min_Amount`, `Credit_Mix`, and other categorical variables.
- Handled skewed/dirty numeric fields by removing special characters and converting types.

## 🔎 Multicollinearity Check

Used `Variance Inflation Factor (VIF)` to check for multicollinearity among numeric features.

## 🤖 Model Training and Evaluation

### ✅ Models Used:

- **Logistic Regression**
  - Basic baseline model for multiclass classification.
- **Decision Tree Classifier**
  - Tuned using `GridSearchCV` for optimal hyperparameters.
- **Random Forest Classifier**
  - Ensemble method for improved accuracy and robustness.

### 📊 Performance Metrics:
- Accuracy is used as the primary evaluation metric.
- Predictions compared against actual values.

### 📌 Final Accuracy:
- **Logistic Regression**: *(Insert accuracy if known)*
- **Decision Tree (Tuned)**: `~Accruracy of Decision Tree Model : xx.xx%` (as printed)
- **Random Forest**: *(Insert accuracy if known)*

## 🧪 Dependencies

Ensure the following Python packages are installed:

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
statsmodels
```

Install all with:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels

```

---

## 🚀 How to Run
1. Clone the repository or copy the code to your local machine.
2. Place the credit_score.csv file in the same directory.
