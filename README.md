# loan-status-prediction
# 🏦 Loan Approval Prediction Model

This project aims to build a machine learning model that predicts whether a loan application will be approved or not. The model utilizes various applicant background information, such as gender, marital status, income, education, and more to make accurate predictions that can assist financial institutions in automating their decision process.

---

## 📁 Dataset Overview

The dataset consists of 13 features that influence loan approval decisions. The target variable is `Loan_Status` (`Y` for approved, `N` for rejected).

### 🔑 Key Features

- **Gender:** Applicant’s gender
- **Married:** Marital status
- **Dependents:** Number of dependents
- **Education:** Education level
- **Self_Employed:** Employment status
- **ApplicantIncome:** Applicant’s income
- **CoapplicantIncome:** Co-applicant’s income
- **LoanAmount:** Requested loan amount
- **Loan_Amount_Term:** Loan repayment term
- **Credit_History:** Credit history (1 = good, 0 = poor)
- **Property_Area:** Area type (Urban, Rural, Semiurban)

---

## 🔄 Machine Learning Lifecycle Followed

### 1. **Data Collection**
- Used historical loan data from a CSV file.

### 2. **Data Cleaning**
- Handled missing values using:
  - `mean()` / `median()` for numerical features
  - `mode()` for categorical features
- Removed inconsistencies and handled outliers using box plots.

### 3. **Exploratory Data Analysis (EDA)**
- Visualized distributions using count plots and histograms.
- Correlation heatmap to assess feature relationships.

### 4. **Feature Engineering**
- Combined incomes into a new column `Total_Income`.
- Applied log transformations to reduce skewness:
  - `ApplicantIncomelog`
  - `LoanAmountlog`
  - `Loan_Amount_Term_log`

### 5. **Data Preparation**
- Label Encoding for categorical variables.
- Train-Test Split: 75% training, 25% testing.

---

## ⚙️ Model Training & Evaluation

The following models were trained and tested:

| Model                    | Accuracy (%) |
|--------------------------|--------------|
| Logistic Regression      | ~81.0        |
| Decision Tree Classifier | ~75.0        |
| Random Forest Classifier | **~83.0**    |
| K-Nearest Neighbors      | ~78.0        |

> Logistic Regression was also evaluated using 5-fold Cross-Validation, with an average score of **~81%**.

---

## 📊 Feature Impact (Hypotheses)

- **Married:** May indicate financial stability.
- **Credit_History:** Strong predictor of repayment reliability.
- **Income:** Higher income typically implies better repayment capability.
- **Dependents:** More dependents may suggest increased financial burden.
- **Education:** Graduates may have better earning potential.

---

## 🚧 Next Steps

- ✅ Clean and preprocess the dataset  
- ✅ Perform exploratory data analysis  
- ✅ Train baseline models  
- 🔜 Hyperparameter tuning (GridSearchCV/RandomizedSearchCV)  
- 🔜 Add more models (e.g., XGBoost, LightGBM)  
- 🔜 Build a Streamlit or Flask-based interface for user interaction  
- 🔜 Model deployment (Docker, Heroku, etc.)

---

## 🚀 How to Run the Notebook

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/loan-approval-prediction.git
   cd loan-approval-prediction
