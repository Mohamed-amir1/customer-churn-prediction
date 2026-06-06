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
- Accuracy: 78.5%  
- ROC-AUC: 0.862  

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| No Churn (0) | 0.91 | 0.79 | 0.84 |
| Churn (1) | 0.57 | 0.78 | 0.66 |

---

### XGBoost
- Accuracy: 76.7%  
- ROC-AUC: 0.858  

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| No Churn (0) | 0.91 | 0.76 | 0.83 |
| Churn (1) | 0.54 | 0.80 | 0.65 |

---

## Final Model Selection
Although Random Forest achieved slightly higher accuracy, XGBoost was selected as the final model due to its strong recall on the churn class, which is more important for identifying customers at risk of leaving.

---

## Explainability (SHAP Analysis - XGBoost)

SHAP was applied to the XGBoost model to interpret predictions globally and locally.
<img width="375" height="624" alt="Screenshot 2026-06-06 203253" src="https://github.com/user-attachments/assets/a6f9370e-9e45-43d7-a730-65830e5a97da" />


###  SHAP Insights:
- Contract type is the most influential feature in churn prediction.
- Month-to-month contracts significantly increase churn probability.
- Low tenure strongly increases churn risk.
- High monthly charges push predictions toward churn.
- Online Security and Tech Support reduce churn probability.

### Interpretation:
- SHAP confirms that churn is mainly driven by **contract flexibility, early customer experience, pricing, and service adoption**.

---

## Visualizations
- Confusion Matrix  
<img width="563" height="735" alt="image" src="https://github.com/user-attachments/assets/a11c0132-8bfd-409b-b6be-6d3b2046e4dc" />

- Churn Distribution  
<img width="552" height="373" alt="image" src="https://github.com/user-attachments/assets/3db4595b-8740-4698-b2f8-59155c2a7d32" />

- Feature Importance Comparison  
<img width="705" height="787" alt="image" src="https://github.com/user-attachments/assets/c0b6b5b8-89aa-4cdf-b259-af0330871dd8" />

---

## Insights (Business Impact)
- Contract type is the strongest driver of churn behavior.
- Month-to-month customers are significantly more likely to churn.
- Higher monthly charges increase churn risk.
- Customers with low tenure are more likely to leave early.
- Online security and tech support services improve customer retention.
- XGBoost focuses more on behavioral features, while Random Forest distributes importance across financial features.

---

## Tools & Technologies
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- XGBoost  
- SHAP  

---

## How to Run
1. Clone the repository  
2. Open the notebook in Jupyter or Google Colab  
3. Run all cells sequentially  

---

## Google Colab
Run the project here:  
https://colab.research.google.com/drive/1MhDEHMH0LdtNAOJ4s8fSW6vtDnA9e1Cc?usp=sharing  

---

## Conclusion
This project demonstrates how machine learning can be used to predict customer churn and support business decision-making.

By analyzing customer behavior and service usage patterns, the models help identify customers at risk of leaving.

Early detection of churn enables businesses to take proactive retention actions such as targeted offers, improved customer support, and personalized engagement strategies, ultimately reducing churn and improving revenue retention.
