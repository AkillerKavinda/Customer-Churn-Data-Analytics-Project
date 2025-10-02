# Customer Churn Analysis

## Overview

Using Python to explore customer churn patterns through visualizations and feature-level analysis, applying univariate and bivariate techniques to uncover insights across gender, partner status, contract type, payment method, tenure, and monthly charges.

## Objectives

- Clean and prepare the dataset for analysis
- Handle missing values and convert data types
- Segment customers based on tenure
- Perform univariate and bivariate analysis
- Visualize churn behavior across categorical and numerical features
- Summarize key insights from the data

## Dataset Overview

The dataset includes customer-level information such as:

- **Demographics**: Gender, SeniorCitizen, Partner, Dependents  
- **Services**: PhoneService, InternetService, OnlineSecurity, TechSupport, StreamingTV, StreamingMovies  
- **Billing**: Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges  
- **Target**: Churn (Yes/No)

## Workflow Summary

- Imported and inspected the dataset
- Converted `TotalCharges` to numeric and handled missing values
- Dropped irrelevant columns (`customerID`, raw `tenure`)
- Binned tenure into 6 groups for segmentation
- Performed univariate analysis using countplots
- Calculated churn rates across feature groups
- Visualized numerical relationships using KDE plots
- Converted categorical variables into dummy variables
- Exported cleaned dataset for further use

## Insights

1. **Gender**: Churn is similar for males and females (26.96% and 26.20%).
2. **Senior Citizens**: Higher churn (41.68%) than non-seniors (23.65%).
3. **Partner**: Female customers without partners are more likely to churn.
4. **Dependents**: Customers without dependents churn more (31.28% vs 15.53%).
5. **Phone Service & Multiple Lines**: No major impact on churn.
6. **Internet Type**: Fiber optic users churn more than DSL or no internet (41.89% vs 19.00% and 7.43%).
7. **Support Services**: Lack of OnlineSecurity, TechSupport, or DeviceProtection leads to higher churn (39–42%).
8. **Streaming Services**: Slightly higher churn without StreamingTV or StreamingMovies (~33% vs ~30%).
9. **Contract Type**: Month-to-month contracts have the highest churn (42.71%), while two-year contracts have the lowest (2.85%).
10. **Paperless Billing**: Users of paperless billing churn more (33.59% vs 16.38%).  
    - Notably, females using Credit Card (automatic) show higher churn.
11. **Payment Method**: Electronic check users churn the most (45.29%), while other methods range from 15–19%.
12. **Tenure**: New customers (1–12 months) have the highest churn (47.68%), dropping to 6.61% for those with 5+ years.
13. **Total Charges**: Total charges increase as monthly charges increase.
14. **Monthly Charges**: Churn is high when monthly charges are high.
15. **Combined Effect**: Customers with high monthly charges and short tenure tend to have low total charges — and this combination is strongly linked to high churn, especially among new users who leave early.

## Output

- Cleaned dataset: `churn_dummy_data.csv`  
- Visualizations for churn behavior  
- Feature-level churn rate summaries

### Tools Used for Output

- **Pandas**: Data manipulation and cleaning  
- **NumPy**: Numerical operations and transformations  
- **Seaborn**: Countplots, KDE plots, and churn rate visualizations  
- **Matplotlib**: Plot customization and layout control
