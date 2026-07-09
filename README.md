# 📊 Customer Churn Analysis

## 📌 Project Overview

Customer churn is a critical business problem for subscription-based and telecom companies. This project performs **Exploratory Data Analysis (EDA)** on telecom customer data to identify customer, contract, tenure, and service characteristics associated with churn.

The analysis was performed using **Python, Pandas, Matplotlib, and Seaborn** and is documented in `TCA.ipynb`.

The objective of this project is to identify meaningful churn patterns and translate them into **data-driven customer retention recommendations**.

---

## 🎯 Business Objective

The primary objectives of this analysis are to:

- Measure the overall customer churn rate.
- Identify customer segments with higher churn.
- Analyze churn across contract types.
- Examine the relationship between tenure and churn.
- Evaluate telecom service attributes associated with churn.
- Identify the strongest churn indicators.
- Provide actionable customer retention recommendations.

---

## 📂 Dataset Summary

| Metric | Value |
|---|---:|
| Total Customers | 7,043 |
| Total Columns | 21 |
| Churned Customers | 1,869 |
| Retained Customers | 5,174 |
| Overall Churn Rate | 26.54% |
| Target Variable | `Churn` |

Each row represents an individual telecom customer.

The dataset contains information related to:

- Customer demographics
- Account tenure
- Phone services
- Internet services
- Online services
- Contract type
- Billing preferences
- Payment methods
- Monthly charges
- Total charges
- Customer churn status

---

## 🧹 Data Quality Checks

The dataset was inspected using:

- `df.info()`
- `df.describe()`
- `df.isnull().sum()`

### Key Data Quality Observations

- Dataset shape was verified as **7,043 rows × 21 columns**.
- No standard null values were identified using `isnull()`.
- `TotalCharges` is stored as an object/string field in the source dataset.
- Blank-string records in `TotalCharges` require explicit handling before numeric analysis or predictive modeling.
- `customerID` represents the customer identifier.
- Duplicate records should be validated using `df.duplicated().sum()` before downstream modeling.

---

## 🔍 Service Attributes Analyzed

The exploratory analysis evaluates churn across the following telecom service attributes:

| Service Attribute | Analysis Focus |
|---|---|
| `PhoneService` | Churn distribution by phone service subscription |
| `MultipleLines` | Churn across multiple-line service categories |
| `InternetService` | DSL, fiber optic, and no internet comparison |
| `OnlineSecurity` | Relationship between security service adoption and churn |
| `OnlineBackup` | Churn differences by backup service adoption |
| `DeviceProtection` | Churn by device protection status |
| `TechSupport` | Relationship between technical support and churn |
| `StreamingTV` | Churn distribution among streaming TV customers |
| `StreamingMovies` | Churn distribution among streaming movie customers |

These attributes were explored using **Seaborn count plots segmented by customer churn status**.

---

# 📈 Churn Analysis

## Overall Customer Churn

The dataset contains:

- **7,043 total customers**
- **1,869 churned customers**
- **5,174 retained customers**

### Overall Churn Rate

**26.54%**

Approximately **one in four customers** in the dataset left the telecom provider.

This indicates a significant customer retention opportunity.

---

## 📄 Churn by Contract Type

Contract duration is one of the strongest churn indicators identified in the dataset.

| Contract Type | Approx. Churn Rate |
|---|---:|
| Month-to-month | 42.7% |
| One year | 11.3% |
| Two year | 2.8% |

### Key Finding

Customers with **month-to-month contracts have substantially higher churn** compared with customers on one-year or two-year contracts.

Longer contract commitments are strongly associated with customer retention.

### Business Implication

The company could target high-risk month-to-month customers with:

- Contract upgrade incentives
- Loyalty benefits
- Discounted annual plans
- Personalized retention offers

---

## 🌐 Churn by Internet Service

| Internet Service | Approx. Churn Rate |
|---|---:|
| Fiber optic | 41.9% |
| DSL | 19.0% |
| No internet service | 7.4% |

### Key Finding

**Fiber optic customers show the highest churn rate among internet service groups.**

This segment should be investigated further for potential issues related to:

- Pricing
- Service reliability
- Customer expectations
- Technical support
- Customer experience

---

## ⏳ Churn by Customer Tenure

The churn distribution indicates that customers with **shorter tenure are more vulnerable to churn**.

Long-tenure customers are more strongly represented among retained customers.

### Key Finding

The early customer lifecycle is a critical retention period.

### Business Implication

The company should prioritize:

- Customer onboarding programs
- Early engagement campaigns
- Proactive customer support
- First-month satisfaction monitoring
- Personalized retention communication

---

# 🚨 Strongest Verified Churn Indicators

Based on the exploratory analysis and dataset distributions, the strongest churn indicators identified are:

### 1. Month-to-Month Contracts

Month-to-month customers have the highest churn rate among contract groups.

### 2. Fiber Optic Internet Service

Fiber optic customers show materially higher churn compared with DSL and customers without internet service.

### 3. Low Customer Tenure

Newer customers demonstrate greater churn vulnerability.

### 4. Lack of Online Security

Customers without `OnlineSecurity` show a higher concentration of churn.

### 5. Lack of Technical Support

Customers without `TechSupport` demonstrate stronger churn patterns.

### 6. Service Bundle and Support Gaps

`OnlineBackup` and `DeviceProtection` provide additional customer segmentation signals for churn analysis.

> **Note:** These findings represent associations identified through exploratory data analysis. They should not be interpreted as proof of causation. Predictive modeling or controlled business experiments would be required for further validation.

---

# 💡 Business Recommendations

Based on the analysis, the following retention strategies are recommended:

### 🎯 Target Month-to-Month Customers

Provide contract upgrade incentives and loyalty offers to encourage longer customer commitments.

### 🌐 Investigate Fiber Optic Customer Experience

Analyze pricing, service reliability, customer complaints, and technical support interactions for fiber optic customers.

### ⏳ Build an Early-Tenure Retention Program

Develop targeted onboarding and engagement strategies for newly acquired customers.

### 🛡️ Promote Support and Security Services

Encourage adoption of:

- Online Security
- Technical Support
- Online Backup
- Device Protection

among high-risk customer segments.

### 🤖 Develop a Churn Prediction Model

The identified churn indicators can be used as candidate features for a future machine learning churn prediction model.

---

# 🔄 Analysis Workflow

1. Imported Python analytics and visualization libraries.
2. Loaded the telecom customer churn dataset.
3. Inspected dataset shape and schema.
4. Performed descriptive statistical analysis.
5. Checked missing values.
6. Analyzed overall customer churn.
7. Segmented churn by customer characteristics.
8. Compared churn across telecom service attributes.
9. Visualized churn patterns using Seaborn and Matplotlib.
10. Translated analytical findings into customer retention recommendations.

---

# 📁 Repository Structure

```text
Customer-Churn-Analysis/
│
├── Customer churn.csv
│   └── Telecom customer churn dataset
│
├── TCA.ipynb
│   └── Python exploratory data analysis notebook
│
├── Telco Customer Churn Analysis.pdf
│   └── Customer churn analysis report
│
└── README.md
    └── Project documentation and business insights
