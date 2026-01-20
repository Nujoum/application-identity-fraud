# Application Identity Fraud Detection  
**Machine Learning for Synthetic Identity and Application Fraud**

This project develops an end-to-end machine learning framework to detect application-level identity fraud, with a focus on synthetic identities and repeated misuse of personal identifiers in financial applications.

---

## Problem Statement
Financial institutions process large volumes of credit and loan applications, where even a small fraud rate can result in significant financial losses. The challenge is to identify high-risk applications efficiently while minimizing operational burden and false positives.

---

## Solution Overview
A supervised machine learning model was built to identify fraudulent applications using identity linkage, velocity, and recency patterns across applicant attributes such as name, SSN, address, phone number, and date of birth.

The approach targets common application fraud behaviors, including:
- Reuse of personal identifiers across multiple applications
- Multiple identities sharing common contact or address information
- Sudden spikes in application activity tied to the same entities

---

## Model Performance (Out-of-Time)
- **Fraud Detection Rate @ 2% (FDR@2%)**: **58.98%**
- Captures a majority of fraudulent applications by reviewing only the top 2% highest-risk cases
- Estimated annual fraud loss reduction of approximately **$32M**, based on modeled business assumptions

The model demonstrates stable performance across training, validation, and out-of-time datasets.

---

## Key Components
- **Feature Engineering**
  - Identity entity construction using combinations of applicant attributes
  - Velocity and recency features across multiple time windows
  - Cross-entity linkage metrics to detect shared or reused identifiers
- **Feature Selection**
  - Initial filtering using Kolmogorov–Smirnov statistics
  - Wrapper-based selection optimized for fraud detection at low review rates
- **Modeling**
  - Gradient boosting model (LightGBM) selected for performance and stability
- **Evaluation**
  - Business-relevant metrics aligned with real-world review constraints
  - Financial impact analysis to determine optimal decision thresholds

---

## Technology Stack
- Python
- LightGBM
- pandas, NumPy, scikit-learn
- Matplotlib / Seaborn

---

## Evaluation Metric
**Fraud Detection Rate at K% (FDR@K%)**  
Measures the proportion of total fraud identified within the top K% of highest-risk scored applications, reflecting operational review capacity.

---

## Data Notes
- The dataset is synthetic and does not contain real personally identifiable information
- Data is designed to reflect realistic fraud patterns for modeling and evaluation purposes

---

## Author
**Nujoum Unus**  
MS in Business Analytics  
