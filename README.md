# 🚗 Car Price Prediction using Machine Learning

This project was completed as part of my Data Science internship at **NOVANECTAR Services Pvt. Ltd.** It focuses on building a regression model that accurately predicts car prices based on various features like engine size, car length, brand, and more.

## 📌 Objective

To clean, analyze, and model a real-world car dataset in order to:
- Identify key features that influence car price.
- Build a predictive model with high accuracy.
- Interpret model results with statistical reasoning.

## 📁 Dataset

The dataset contains specifications of various cars along with their prices. It was originally provided as part of the internship task.

**Key Columns:**
- `CarName`
- `enginesize`
- `carlength`
- `carwidth`
- `curbweight`
- `carbody`, `fueltype`, etc.
- `price` (Target Variable)

## 🛠️ Technologies Used

- **Python 3.10+**
- **Pandas** & **NumPy** – Data preprocessing
- **Seaborn** & **Matplotlib** – Visualization
- **Scikit-learn** – Feature scaling & selection
- **Statsmodels** – Regression modeling
- **Jupyter Notebook** – Development environment

## ⚙️ Key Steps in Workflow

1. **Data Cleaning**
   - Null value handling
   - Categorical corrections (e.g., fixing car brand typos)
   - Removing multicollinear features

2. **Feature Engineering**
   - Extracted car brand from `CarName`
   - Dummy encoding of categorical features
   - Created derived feature: `car_stability`

3. **Visualization**
   - Pairplot and heatmap to assess relationships
   - Identified redundant and highly correlated variables

4. **Feature Selection**
   - Scaled numerical features using `MinMaxScaler`
   - Applied RFE (Recursive Feature Elimination) to choose top 15 features

5. **Model Building**
   - Built a linear regression model using `statsmodels.OLS`
   - Evaluated using R², Adjusted R², RMSE

6. **Model Evaluation**
   - Residual analysis to validate model assumptions
   - Final prediction on test data

## 📈 Results

- **R² Score (Test Set):** ~0.902
- **RMSE:** ~0.072
- **Important Predictors:** `enginesize`, `carlength`, car brand (e.g., `bmw`, `buick`), `cylindernumber`

## 📊 Final Model Equation (Simplified)

```text
Price = 0.2578 * carlength + 0.6109 * enginesize + 
        0.01969 * bmw + 0.1800 * buick + 0.3035 * porsche - 
        0.0942 * four_cylinders
