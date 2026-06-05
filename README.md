# Customer Churn Prediction

## Project Overview
Customer churn is one of the most important business problems in subscription-based companies. This project uses machine learning to predict whether a customer is likely to leave the company based on demographic information, services used, and account details.

The goal is to help businesses identify at-risk customers and improve customer retention strategies.

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
- Handling missing values in TotalCharges
- Converting TotalCharges to numeric format
- Encoding categorical variables
- Removing unnecessary columns (customerID)
- Train-test split

---

## Models Used

### 1. Random Forest Classifier
- 500 trees
- Max depth = 10
- Balanced class weights
- Random state = 42

### 2. XGBoost Classifier
- n_estimators = 280
- max_depth = 4
- learning rate = 0.05
- scale_pos_weight for class imbalance

---

## Model Performance

### Random Forest
Accuracy: 78.5%

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| No Churn (0) | 0.91 | 0.79 | 0.84 |
| Churn (1) | 0.57 | 0.78 | 0.66 |

---

### XGBoost
Accuracy: 76.7%

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| No Churn (0) | 0.91 | 0.76 | 0.83 |
| Churn (1) | 0.54 | 0.80 | 0.65 |

---

## Final Model Selection
Although Random Forest achieved slightly higher accuracy, XGBoost was selected as the final model due to its better recall on the churn class, which is more important for identifying customers at risk of leaving.

---

## Visualizations
- Confusion Matrix
<img width="563" height="735" alt="image" src="https://github.com/user-attachments/assets/a11c0132-8bfd-409b-b6be-6d3b2046e4dc" />
  

- Churn Distribution
<img width="552" height="373" alt="image" src="https://github.com/user-attachments/assets/3db4595b-8740-4698-b2f8-59155c2a7d32" />
  

- Feature Importance Analysis (Random Forest and XGBoost comparison)
<img width="705" height="787" alt="image" src="https://github.com/user-attachments/assets/c0b6b5b8-89aa-4cdf-b259-af0330871dd8" />
  

---

## Key Insights
- Contract type is the most influential factor in customer churn.
- Month-to-month customers are significantly more likely to churn than long-term contract customers.
- Higher monthly charges are associated with increased churn risk.
- Customers with lower tenure are more likely to leave.
- Online security and tech support services strongly reduce churn probability.
- XGBoost focuses more on behavioral features, while Random Forest distributes importance across financial features as well.

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

## How to Run
1. Clone the repository
2. Open the notebook in Jupyter or Google Colab
3. Run all cells sequentially

---
## Google Colab

You can run this project directly on Google Colab without any local setup:

[[Open in Google Colab](https://colab.research.google.com/)](https://colab.research.google.com/drive/1MhDEHMH0LdtNAOJ4s8fSW6vtDnA9e1Cc?usp=sharing)
---

## Conclusion
This project demonstrates how machine learning can be used to predict customer churn and support business decision-making.

By analyzing customer behavior and service usage patterns, the models help identify customers at risk of leaving.

Early detection of churn enables businesses to take proactive retention actions such as targeted offers, improved customer support, and personalized engagement strategies, ultimately improving customer retention and reducing revenue loss.
