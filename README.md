# 📊 Customer Churn Analysis

## Project Overview

Customer churn directly impacts recurring revenue, customer acquisition costs, and long-term business growth.

This project performs **Exploratory Data Analysis (EDA)** on a telecom customer dataset to identify customer segments and service characteristics associated with higher churn.

Using **Python, Pandas, Matplotlib, and Seaborn**, I analyzed customer tenure, contract type, internet service, and telecom service subscriptions to identify meaningful churn patterns and translate them into actionable retention recommendations.

---

## 🎯 Business Objective

The analysis focuses on answering four key business questions:

- What percentage of customers are churning?
- Which customer segments have the highest churn risk?
- Which contract and service attributes are associated with churn?
- What retention actions could the business prioritize?

---

## 📊 Dataset Snapshot

| KPI | Result |
|---|---:|
| Total Customers | 7,043 |
| Total Features | 21 |
| Churned Customers | 1,869 |
| Retained Customers | 5,174 |
| Overall Churn Rate | 26.54% |
| Duplicate Rows | 0 |
| Target Variable | `Churn` |

Each row represents one telecom customer and contains demographic, account, service, contract, billing, and churn information.

---

## 🔍 Key Churn Findings

### 1. Overall Churn Rate — 26.54%

Out of **7,043 customers, 1,869 customers churned**.

Approximately **1 in 4 customers left the telecom provider**, highlighting a significant customer retention opportunity.

---

### 2. Month-to-Month Customers Are the Highest-Risk Contract Segment

| Contract Type | Churn Rate |
|---|---:|
| Month-to-month | 42.7% |
| One year | 11.3% |
| Two year | 2.8% |

Customers on **month-to-month contracts churn at a substantially higher rate** than customers with longer-term contracts.

**Business implication:** Retention campaigns should prioritize month-to-month customers and encourage migration toward annual contracts through loyalty benefits or contract incentives.

---

### 3. Fiber Optic Customers Show Elevated Churn

| Internet Service | Churn Rate |
|---|---:|
| Fiber optic | 41.9% |
| DSL | 19.0% |
| No internet service | 7.4% |

Fiber optic customers recorded the **highest churn rate among internet service groups**.

**Business implication:** The business should investigate fiber optic customer experience, including pricing, service reliability, support interactions, and customer expectations.

---

### 4. Online Security Is Associated With Lower Churn

| Online Security | Churn Rate |
|---|---:|
| No | 41.8% |
| Yes | 14.6% |
| No internet service | 7.4% |

Customers without Online Security show a considerably higher churn rate than customers subscribed to the service.

**Business implication:** Online Security adoption can be used as a customer segmentation signal when identifying high-risk accounts.

---

### 5. Technical Support Shows a Strong Churn Pattern

| Technical Support | Churn Rate |
|---|---:|
| No | 41.6% |
| Yes | 15.2% |
| No internet service | 7.4% |

Customers without Tech Support demonstrate substantially higher churn.

**Business implication:** Proactive support programs and targeted technical assistance may help improve customer retention.

---

### 6. Short-Tenure Customers Are More Vulnerable to Churn

Exploratory analysis indicates that churn is concentrated more heavily among customers with **shorter account tenure**.

Customers with longer tenure are more strongly represented among retained customers.

**Business implication:** The early customer lifecycle is a critical retention window. New customers should receive stronger onboarding, proactive support, and early engagement.

---

## 🛠️ Service Attributes Analyzed

The analysis evaluated churn patterns across nine telecom service attributes:

| Service Attribute | Analytical Focus |
|---|---|
| `PhoneService` | Phone service subscription and churn |
| `MultipleLines` | Multiple-line service categories |
| `InternetService` | DSL, fiber optic, and no internet |
| `OnlineSecurity` | Security service adoption |
| `OnlineBackup` | Backup service adoption |
| `DeviceProtection` | Device protection subscription |
| `TechSupport` | Technical support availability |
| `StreamingTV` | Streaming TV subscription |
| `StreamingMovies` | Streaming movie subscription |

Churn distributions were explored using **Seaborn count plots segmented by `Churn` status**.

---

## 🧹 Data Quality Assessment

The dataset was inspected using:

```python
df.info()
df.describe()
df.isnull().sum()
df.duplicated().sum()
