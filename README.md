# Customer Churn Prediction and Analysis 📉

## 📘 Project Overview

This project focuses on analyzing and predicting **customer churn** for a telecommunications company.  
Customer churn is defined as a customer canceling their subscription.  
The primary goal is to build a robust **machine learning model** that accurately identifies customers likely to churn and to provide actionable business recommendations based on the key drivers of churn.

---

## 📊 Dataset and Goal

- **Dataset:** Contains 7,043 customer records with 21 features.  
- **Features:** Include customer demographics (gender, age), account information (tenure, contract type), and subscribed services (internet, phone, streaming).  
- **Target Variable:** `Churn` (Yes/No).

---

## ⚙️ Methodology

This project follows a complete **Machine Learning Workflow**:

1. **Data Cleaning and Preprocessing:**  
   Handled missing values, standardized data types, and ensured proper formatting.

2. **Exploratory Data Analysis (EDA):**  
   Visualized relationships between key variables (e.g., tenure, contract type, monthly charges) and the target variable `Churn`.

3. **Feature Engineering & Scaling:**  
   Applied `ColumnTransformer` and `Pipeline` for efficient preprocessing:
   - Numerical features (`MonthlyCharges`, `TotalCharges`, `tenure`) scaled using `StandardScaler`.  
   - Categorical features encoded using `OneHotEncoder`.

4. **Model Building:**  
   Implemented and compared multiple classification algorithms:
   - **Logistic Regression**  
   - **Random Forest Classifier**

5. **Model Evaluation:**  
   Evaluated models using:
   - `classification_report`  
   - `confusion_matrix`  
   - `accuracy_score`

---

## 🧮 Data Preparation Steps

Key preprocessing steps before modeling:

- The `TotalCharges` column (originally of type `object` with missing spaces) was cleaned by replacing spaces with `0` and converting it to a numeric (`float`) type.  
- The binary column `SeniorCitizen` (`0`/`1`) was converted to categorical (`"yes"`/`"no"`) for interpretability.  
- Verified no null or duplicate entries remained before model training.

---

## 💡 Key Findings and Business Recommendations

The analysis identified major churn drivers and proposed targeted retention strategies:

### 1. **Address New Customer Risk**
- **Finding:** Churn risk is highest during the first few months of tenure.  
- **Recommendation:** Implement proactive customer engagement (e.g., welcome support calls or discount offers) during this initial period.

### 2. **Incentivize Longer Contracts**
- **Finding:** Month-to-month contracts show the highest churn rates.  
- **Recommendation:** Offer incentives for customers to shift to **1- or 2-year contracts** — such as bundled services or discounted monthly rates.

### 3. **Ensure Premium Service Quality**
- **Finding:** Customers paying higher monthly charges are more likely to churn.  
- **Recommendation:** Improve perceived value by ensuring strong service reliability and responsive customer support for premium plans.

### 4. **Investigate Payment Method**
- **Finding:** The **Electronic Check** payment method correlates with higher churn.  
- **Recommendation:** Review and improve the payment experience for this method to reduce potential friction.

---

## 🧰 Dependencies

This project requires Python and the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Libraries used:
- pandas – data manipulation
- numpy – numerical operations
- matplotlib & seaborn – data visualization
- scikit-learn – preprocessing, model training, and evaluation

🚀 How to Run the Project
1. Clone the repository:
```bash
git clone [your-repo-link]
```
2. Add the dataset:
Place Customer Churn.csv in the same directory as the notebook.

3. Run the notebook:
Open the Jupyter Notebook (Customer_Churn_Prediction.ipynb) and execute all cells sequentially.

🧾 Author & Acknowledgment

Developed with ❤️ using Python and open-source machine learning tools.
Dataset sourced from a publicly available Telco Customer Churn dataset, commonly used in data science case studies.
