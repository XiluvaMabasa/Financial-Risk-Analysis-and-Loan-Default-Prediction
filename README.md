# Financial-Risk-Analysis-and-Loan-Default-Prediction

### Project Overview
Financial institutions must assess borrower risk to minimize losses and improve lending decisions. Analysis of customer data to identify key drivers of credit risk and build machine learning models to predict the likelihood of loan default.

### Objectives
- Analyze patterns in customer financial behavior
- Identify key factors influencing credit risk
- Perform SQL-based analysis to extract business insights
- Build an evaluate machine learning models to predict default risk

### Tools & Technologies
- Python (Pandas, NumPy, Scikit-learn)
- SQL (SQLite) for querying and analysis
- Power BI for data visualization
- Machine Learning(Logistic Regression, Random Forest)

### Dataset
- German Credit Risk Dataset
- Contains customer demographic and financial information such as:
    - Age
    - Job
    - Housing
    - Credit amount
    - Loan duration
    - Account status
    - Risk (Good/Bad)

 ### Data Cleaning & Preparation
 - Handled missing values in account-related features
 - Encoded categorical variables for modeling
 - Standardised features for Logistic Regression
 - Revomed unnecessary columns (e.g., index column)

### Feature Engineering
To better capture financial behavior, new features were created:
- Credit per Month- Measures repayment burden
- Duration Groups- Categorizes loan terms
- Age Groups- Segments customers by life stage
- High Credit Risk- Identifies large loans
These features improved model performance and interpretability.

### SQL Analysis (Key Business Questions)
#### 1. What is the distribution of risk?
- ~70% low-risk vs 30% high-risk customers
- Reflects real-world class imbalance in lending

#### 2. Do high-risk customers borrow more?
- High-risk customers have a higher average credit amount

#### 3. Does loan duration affect risk?
- Longer loan durations are associated with higher default risk

#### 4. Does housing status influence risk?
- Customers in free housing show a higher risk compared to homeowners

#### 5. Does repayment burden affect risk?
- Credit burden shows a non-linear relationship with risk

### Machine Learning Models
#### 1. Logistic Regression
- Baseline model
- Improved using class_weight='balanced' to handle class imbalance

#### 2. Random Forest
- Non-lineae model for comparison

### Model Performance
1. Logistic regression
   - Accuracy: 78% to 68%
   - Recall (High Risk): 44% to 63%
  
2. Random Forest
   - Accuracy: 77%
   - Recall: 39%
  
#### Key Insight:
- Logistic Regression performed better in identifying high-risk customers
- Recall improved significantly after handling class imbalance

### Business Interpretation
In financial risk modeling:
- Missing a risky customer = high financial loss
- Incorrectly flagging a safe customer = lower cost
Therefore, recall is prioritized over accuracy

### Key Insights
- Loan duration is a major driver of risk - longer loans increase default likelihood
- Repayment burden (credit per month) is a strong predictor of financial stress
- Higher loan amounts are associated with higher risk
- Housing stability influences creditworthiness
- Employment type (job) impacts financial stability

### Feature Importance
Top predictor of risk:
- Duration
- Credit per month
- Duration groups
- Job
These highlight the importance of loan structure and borrower stability in risk assessment.

### Dashboard
The dashboard provides:
- Risk distribution
- Financial behavior insights
- Customer segmentation
  

### Conclusion
This project demonstrates a full end-to-end financial analytics overflow:
- Data cleaning and feature engineering
- SQL-based business analysis
- Machine learning modeling and evaluation
The results show that loan structure and repayment burden are key drivers of credit risk, and that optimizing for recall improves the detection of high-risk customers.

### Future Improvements
- Hyperparameter tuning for improved model performance
- Use of advanced models (e.g., XGBoost)
- Deployment via Streamlit for real-time risk prediction

### Author
#### Xiluva Mabasa
