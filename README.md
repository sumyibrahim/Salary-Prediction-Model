# **Salary Prediction Model**

## **Project Overview**
This project builds a machine learning model to predict salaries (`salary_in_usd`) based on key factors such as job title, experience level, remote ratio, company size, and company location. The goal is to help organizations and professionals estimate salary ranges based on these features. 

Multiple machine learning algorithms were implemented, evaluated, and compared to identify the most effective model for salary prediction.

---

## **Dataset**
- **Size**: 16,494 rows, 7 columns
- **Source**: [Specify source if available, or write "Simulated data for this project"]
- **Features**:
  1. `work_year`: Year of the job record.
  2. `experience_level`: Level of job experience (e.g., Junior, Mid-level, Senior).
  3. `job_title`: The job designation.
  4. `salary_in_usd`: Annual salary in USD (target variable).
  5. `remote_ratio`: Percentage of remote work (0–100).
  6. `company_location`: Location of the company.
  7. `company_size`: Size of the company (Small, Medium, Large).

Outliers in the salary column were handled by **capping values** within the interquartile range (IQR) to ensure more robust model performance.

---

## **Models and Performance**
The following machine learning models were trained and evaluated using RMSE (Root Mean Square Error) and R² (coefficient of determination):

| **Model**                | **Training R²** | **Test R²** | **RMSE**          |
|--------------------------|-----------------|-------------|-------------------|
| **Linear Regression**     | 25.06%          | 24.83%      | 59,087            |
| **Random Forest**         | 32.13%          | 25.24%      | 59,523            |
| **Decision Tree**         | 32.50%          | 22.62%      | 60,479            |
| **Support Vector Regressor (SVR)** | -0.94%         | -0.46%     | 68,617            |
| **XGBoost**               | 31.81%          | 26.52%      | 59,374            |

### **Best Performing Model**
The **XGBoost model** emerged as the most effective, with:
- **Training R²**: 31.81%
- **Test R²**: 26.52%
- **RMSE**: $59,374

---

## **Technologies Used**
- **Programming Language**: Python
- **Libraries**:
  - **Data Analysis**: pandas, numpy
  - **Visualization**: matplotlib, seaborn
  - **Machine Learning**: scikit-learn, XGBoost
- **Environment**: Jupyter Notebook / Google Colab

---

## **Key Features**
1. **Outlier Capping**: Ensures the model handles extreme salary values without biasing predictions.
2. **Model Comparison**: Evaluated both simple (Linear Regression) and advanced (XGBoost) models.
3. **Interpretability**: Provides insights into the impact of different features on salary predictions.

---

## **Next Steps**
1. **Feature Engineering**: Add more relevant features, such as industry, education level, or skills.
2. **Hyperparameter Tuning**: Further optimize models to improve performance.
3. **Deployment**: Deploy the model as a web app (e.g., Flask or Streamlit) for real-world use.

---

## **Usage Instructions**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/salary-prediction-model.git
