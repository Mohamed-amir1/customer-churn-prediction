# Customer Churn Prediction

## Project Overview
Customer churn is one of the most important business problems in subscription-based companies. This project uses machine learning to predict whether a customer is likely to leave the company based on demographic information, services used, and account details.

The goal is to help businesses identify at-risk customers and improve retention strategies.

---

## Dataset Description
The dataset contains customer information such as:
- Gender
- Senior Citizen Status
- Partner
- Dependents
- Tenure
- Phone Service
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Tech Support
- Streaming TV
- Streaming Movies
- Contract Type
- Paperless Billing
- Payment Method
- Monthly Charges
- Total Charges

---

## Target Variable
- Churn = 1 → Customer left the company
- Churn = 0 → Customer stayed

---

## Data Preprocessing
- Handling missing values
- Converting TotalCharges to numeric format
- Encoding categorical variables
- Removing unnecessary columns
- Train-test split

---

## Model Used
Random Forest Classifier:
- 500 trees
- Max depth = 10
- Balanced class weights
- Random state = 42

---

## Model Performance

### Accuracy
79%

### Classification Report

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| No Churn (0) | 0.91 | 0.80 | 0.85 |
| Churn (1) | 0.58 | 0.78 | 0.66 |

The model performs better at identifying churned customers due to relatively high recall for class 1.

---

## Visualizations
- Confusion Matrix
  
<img width="577" height="392" alt="image" src="https://github.com/user-attachments/assets/5080efad-f9db-40cb-97cf-90e870d130c8" />

- Churn Distribution

<img width="616" height="446" alt="image" src="https://github.com/user-attachments/assets/e0993c0f-20ad-49ed-be33-b4a7dd269e20" />
  
- Feature Importance Analysis

<img width="795" height="466" alt="image" src="https://github.com/user-attachments/assets/820a8f66-ca8e-41b8-a9a6-c58e27b707be" />

---

## Key Insights
- Contract type is a strong predictor of churn
- Month-to-month customers are more likely to leave
- Higher monthly charges increase churn probability
- Retention strategies should focus on high-risk segments

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## How to Run
1. Clone the repository
2. Open the Customer_Churn in Jupyter or Google Colab
3. Run all cells



---

## Conclusion
This project demonstrates how machine learning can be used to predict customer churn and support business decision-making. It helps identify customers at risk and enables proactive retention strategies.
