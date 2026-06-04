# 📉 Customer Churn Prediction

## 📌 Project Overview

Customer churn is one of the most important business challenges for subscription-based companies. This project uses Machine Learning to predict whether a customer is likely to leave the company based on demographic information, services used, and account details.

The goal is to help businesses identify at-risk customers and improve customer retention strategies.

---

## 📊 Dataset Description

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

### 🎯 Target Variable

- **Churn = 1** → Customer left the company
- **Churn = 0** → Customer stayed with the company

---

## 🧹 Data Preprocessing

The following preprocessing steps were applied:

- Handling missing values
- Converting TotalCharges to numeric format
- Encoding categorical variables
- Removing unnecessary columns
- Train-Test Split

---

## 🤖 Model Used

### Random Forest Classifier

The model was trained using:

- 500 Trees
- Maximum Depth = 10
- Balanced Class Weights
- Random State = 42

---

## 📈 Model Performance

### Accuracy

**79%**

### Classification Report

| Class | Precision | Recall | F1-Score |
|---------|---------|---------|---------|
| No Churn (0) | 0.91 | 0.80 | 0.85 |
| Churn (1) | 0.58 | 0.78 | 0.66 |

The model performs well in identifying customers at risk of churn, achieving a recall score of 78% for churned customers.

---

## 📊 Visualizations

### Confusion Matrix

<img width="577" height="392" alt="image" src="https://github.com/user-attachments/assets/5080efad-f9db-40cb-97cf-90e870d130c8" />

### Churn Distribution

<img width="616" height="446" alt="image" src="https://github.com/user-attachments/assets/e0993c0f-20ad-49ed-be33-b4a7dd269e20" />


### Top 10 Important Features

<img width="795" height="466" alt="image" src="https://github.com/user-attachments/assets/820a8f66-ca8e-41b8-a9a6-c58e27b707be" />


---

## 🔍 Key Insights

- Contract type is one of the strongest predictors of customer churn.
- Customers with month-to-month contracts are more likely to leave.
- Customers with higher monthly charges show a higher tendency to churn.
- Customer retention efforts should focus on high-risk customer segments.

---

## 🧰 Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---



## 🚀 How to Run

1. Clone the repository

2. Open the notebook in Jupyter Notebook or Google Colab

3. Run all cells

---

## 📁 Project Structure

```
Customer-Churn/
│
├── Customer-Churn.csv
├── Customer_Churn.ipynb
├── README.md
└── Requirements.txt
```

---

## 🏁 Conclusion

This project demonstrates how machine learning can be used to predict customer churn and support business decision-making. By identifying customers who are likely to leave, companies can take proactive actions to improve customer retention and reduce revenue loss.
