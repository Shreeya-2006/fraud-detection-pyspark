# Financial Fraud Detection System using PySpark

## Project Overview

This project presents an end-to-end **financial fraud detection system** built using PySpark and Machine Learning techniques. The objective is to identify fraudulent credit card transactions from a highly imbalanced dataset and improve detection performance while balancing false positives.

The project also includes a **Power BI dashboard** to visualize model performance and business insights, making it suitable for real-world financial analytics applications.

---

## Problem Statement

Fraud detection is a critical challenge in financial systems due to the **extreme class imbalance**—fraudulent transactions represent less than 1% of total data. Traditional models often achieve high accuracy but fail to detect actual fraud cases effectively.

---

## Approach & Methodology

### Data Processing

* Used **PySpark** for scalable data handling
* Loaded and explored dataset containing 284,807 transactions
* Verified data quality (no missing values)

---

### Feature Engineering

* Selected relevant features (`Time`, `V1–V28`, `Amount`)
* Used **VectorAssembler** to combine features into a single vector for ML models

---

### Model Development

* Implemented **Logistic Regression** using PySpark ML
* Split dataset into training (80%) and testing (20%)

---

### Handling Class Imbalance

* Observed severe imbalance (~0.17% fraud cases)
* Applied **class weighting technique**
* Increased importance of fraud transactions during training

---

### Model Evaluation

* Used **AUC (Area Under Curve)** as primary evaluation metric
* Compared performance before and after handling imbalance

---

## Results & Performance

### Before Optimization

* Fraud Detection Rate: ~65%
* Missed Fraud Cases: 32
* AUC Score: 0.96

---

### After Optimization (Weighted Model)

* Fraud Detection Rate: **~90%**
* Missed Fraud Cases: **9**
* AUC Score: **0.98**

---

## Trade-off Analysis

Improving fraud detection led to an increase in false positives:

* False Positives: **1340**

This trade-off is common in fraud detection systems where minimizing missed fraud is prioritized over reducing false alarms.

---

## Power BI Dashboard

A professional dashboard was created to visualize:

* Fraud detected
* Missed fraud cases
* False positives
* Overall model performance

The dashboard helps translate technical results into **business insights**.

---

## Tech Stack

* **Python**
* **PySpark**
* **Machine Learning (Logistic Regression)**
* **Power BI**

---

## Project Structure

```
Fraud-Detection-System/
│
├── fraud_detection.ipynb
├── fraud_results.xls
├── dashboard.png
├── README.md
```

---

## Dataset

* Credit Card Fraud Detection Dataset
* Total transactions: 284,807
* Fraud cases: 492 (~0.17%)

Dataset Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

## Key Learnings

* Handling imbalanced datasets is crucial for fraud detection
* High accuracy alone is not a reliable metric
* AUC provides better evaluation for skewed data
* Class weighting significantly improves fraud detection
* Visualization bridges the gap between technical results and business understanding

---

## Future Improvements

* Implement advanced models (Random Forest, Gradient Boosting)
* Optimize classification threshold to reduce false positives
* Deploy model as a real-time fraud detection API
* Integrate streaming data using Spark Streaming

---

## Business Impact

This system demonstrates how machine learning can be used to:

* Reduce financial fraud losses
* Improve detection accuracy
* Support decision-making with clear visual insights

---

## Author

Shreeya Phapale
