# 📊 Customer Churn Analysis

## 📌 Project Overview

Customer churn is one of the major challenges faced by subscription-based businesses. Understanding **which customers are more likely to churn and what characteristics are associated with churn** can help businesses improve customer retention and reduce revenue loss.

This project performs an **Exploratory Data Analysis (EDA)** on a customer churn dataset to identify patterns and relationships between customer characteristics, services, contracts, payment methods, tenure, charges, and churn behavior.

The analysis was performed using **Python, Pandas, Matplotlib, and Seaborn**, with a focus on data cleaning, descriptive analysis, and visualization.

---

## 🎯 Project Objective

The main objective of this project is to analyze customer churn and answer questions such as:

- What percentage of customers have churned?
- Which customer groups show higher churn?
- Does customer tenure have a relationship with churn?
- Which contract types are associated with higher churn?
- Which internet service users show greater churn?
- Does the use of additional services relate to customer retention?
- Which payment methods are associated with higher churn?
- What customer segments should businesses focus on for retention?

---

## 📂 Dataset

The dataset contains **7,043 customer records and 21 attributes**.

### Key Features

| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `gender` | Customer gender |
| `SeniorCitizen` | Whether the customer is a senior citizen |
| `Partner` | Whether the customer has a partner |
| `Dependents` | Whether the customer has dependents |
| `tenure` | Number of months the customer has been with the company |
| `PhoneService` | Whether phone service is subscribed |
| `MultipleLines` | Multiple phone lines subscription |
| `InternetService` | Type of internet service |
| `OnlineSecurity` | Online security subscription |
| `OnlineBackup` | Online backup subscription |
| `DeviceProtection` | Device protection subscription |
| `TechSupport` | Technical support subscription |
| `StreamingTV` | Streaming TV subscription |
| `StreamingMovies` | Streaming movies subscription |
| `Contract` | Contract type |
| `PaperlessBilling` | Whether paperless billing is enabled |
| `PaymentMethod` | Customer payment method |
| `MonthlyCharges` | Monthly amount charged |
| `TotalCharges` | Total amount charged |
| `Churn` | Whether the customer left the company |

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Jupyter Notebook**

---

## 🔍 Data Cleaning & Preparation

Before performing the analysis, the dataset was inspected and cleaned.

### Steps performed:

1. Loaded the CSV dataset using Pandas.
2. Inspected the dataset structure using `df.info()`.
3. Checked for missing/null values.
4. Identified blank values in the `TotalCharges` column.
5. Replaced blank `TotalCharges` values with `0`.
6. Converted `TotalCharges` from string to numeric format.
7. Checked for duplicate records.
8. Checked for duplicate `customerID` values.
9. Converted the `SeniorCitizen` binary values (`0` and `1`) into more readable `yes`/`no` categories.

### Data Quality Results

- **Rows:** 7,043
- **Columns:** 21
- **Null values:** 0 after cleaning
- **Duplicate rows:** 0
- **Duplicate customer IDs:** 0

The dataset therefore provides a clean basis for exploratory analysis.

---

# 📈 Exploratory Data Analysis

The project uses several visualizations to understand the relationship between customer attributes and churn.

## 1. Overall Customer Churn

A countplot and pie chart were used to understand the overall distribution of customers who stayed versus those who churned.

### Key Finding

Approximately **26.5% of customers have churned**, while approximately **73.5% have remained with the company**.

This indicates that although the majority of customers are retained, churn represents a significant portion of the customer base and therefore deserves attention.

---

## 2. Churn by Gender

Customer churn was compared across male and female customers.

The analysis does not show gender as the primary differentiating factor in the churn patterns. Therefore, customer retention strategies should not rely heavily on gender alone.

---

## 3. Senior Citizens and Churn

The analysis compares churn between senior citizens and non-senior customers.

The visualization indicates that **senior citizens have a comparatively higher tendency to churn**.

This suggests that senior customers may represent an important segment for targeted retention initiatives.

---

## 4. Tenure and Churn

Customer tenure was analyzed using a histogram with churn as a grouping variable.

### Key Finding

Customers with **shorter tenure**, particularly those in the early months of their relationship with the company, show a higher tendency to churn.

Customers with longer tenure demonstrate stronger retention.

This highlights the importance of the **early customer lifecycle**. Businesses may benefit from improving onboarding, customer support, and engagement during the first few months.

> **Important:** The analysis identifies an association between tenure and churn; it does not establish that short tenure directly causes churn.

---

## 5. Contract Type and Churn

Customer churn was analyzed across:

- Month-to-month
- One-year
- Two-year contracts

### Key Finding

Customers on **month-to-month contracts show a substantially higher tendency to churn** compared with customers on one-year and two-year contracts.

Longer-term contracts appear to be associated with stronger customer retention.

### Business Implication

Businesses could consider strategies such as:

- Incentives for longer-term contracts
- Discounts for annual plans
- Contract upgrade campaigns
- Personalized offers for month-to-month customers

---

## 6. Internet Service and Churn

Churn was compared across different internet service categories.

### Key Finding

Customers using **Fiber optic internet show a particularly high number of churned customers** compared with DSL and customers without internet service.

This makes Fiber optic customers an important segment for further investigation.

Possible areas for deeper analysis include:

- Pricing
- Service quality
- Customer support
- Technical issues
- Competitor pricing
- Additional service adoption

---

## 7. Additional Services and Churn

The project analyzes several additional services:

- Online Security
- Online Backup
- Device Protection
- Tech Support
- Streaming TV
- Streaming Movies

### Key Finding

Customers **without Online Security, Online Backup, Device Protection, and Tech Support consistently show higher churn patterns** than customers who have these services.

The differences for Streaming TV and Streaming Movies appear comparatively smaller.

### Business Implication

Additional services may contribute to stronger customer engagement and perceived value. Businesses could investigate whether bundling or promoting these services can improve retention.

---

## 8. Phone Service and Churn

The analysis compares customers with and without phone service.

Most customers have phone service, and the visualization shows noticeable churn within this group.

However, because the underlying customer groups are not equal in size, **category-level churn rates should be considered alongside raw churn counts** before making business decisions.

---

## 9. Payment Method and Churn

Customer churn was analyzed based on payment method.

### Key Finding

Customers using **Electronic Check show a higher tendency to churn** compared with customers using other payment methods.

### Business Implication

The company could investigate whether payment friction or customer behavior associated with electronic checks contributes to churn and consider encouraging customers to use automatic payment methods.

---

# 💰 Customer Charges

The descriptive analysis provides an overview of customer tenure and charges.

| Metric | Value |
|---|---:|
| Average Tenure | 32.37 months |
| Median Tenure | 29 months |
| Minimum Tenure | 0 months |
| Maximum Tenure | 72 months |
| Average Monthly Charges | 64.76 |
| Median Monthly Charges | 70.35 |
| Minimum Monthly Charges | 18.25 |
| Maximum Monthly Charges | 118.75 |
| Average Total Charges | 2,279.73 |
| Median Total Charges | 1,394.55 |
| Maximum Total Charges | 8,684.80 |

These statistics show considerable variation in both customer tenure and spending.

---

# 📊 Key Insights

The exploratory analysis highlights several important customer segments associated with churn:

| Customer Characteristic | Churn Pattern |
|---|---|
| Overall customer base | ~26.5% churn |
| Short-tenure customers | Higher churn tendency |
| Month-to-month contracts | Higher churn tendency |
| Senior citizens | Comparatively higher churn |
| Fiber optic users | High churn concentration |
| No Online Security | Higher churn pattern |
| No Online Backup | Higher churn pattern |
| No Device Protection | Higher churn pattern |
| No Tech Support | Higher churn pattern |
| Electronic Check users | Higher churn tendency |

These findings are based on exploratory visual analysis and should be interpreted as **relationships/associations rather than causal conclusions**.

---

# 💡 Business Recommendations

Based on the analysis, the following strategies could help improve customer retention:

### 1. Focus on New Customers

Customers in the early stages of their relationship show stronger churn tendencies.

Businesses should focus on:

- Better onboarding
- Early engagement
- Proactive customer support
- Welcome offers
- Early satisfaction checks

### 2. Encourage Long-Term Contracts

Month-to-month customers represent a higher-risk segment.

Possible strategies include:

- Annual-plan discounts
- Loyalty benefits
- Contract upgrade incentives
- Personalized renewal offers

### 3. Investigate Fiber Optic Churn

Fiber optic customers show a particularly high number of churned customers.

The company should investigate whether this is related to:

- Pricing
- Service quality
- Technical issues
- Customer support
- Competitor offerings

### 4. Promote Value-Added Services

Customers without services such as Online Security, Online Backup, Device Protection, and Tech Support show higher churn patterns.

Bundling these services could potentially increase customer engagement and perceived value.

### 5. Review Payment Behavior

Electronic Check users show higher churn tendencies.

The company could evaluate payment experience and encourage convenient automatic payment options.

### 6. Develop Customer Risk Segmentation

Instead of looking at individual factors separately, businesses could combine characteristics such as:

**Short tenure + Month-to-month contract + Fiber optic + Electronic Check + No additional services**

to identify potentially high-risk customer segments.

---

# 📁 Project Structure

```text
Customer-Churn-Analysis/
│
├── churn.ipynb
├── customer_churn.csv
└── README.md
```

---

# 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/customer-churn-analysis.git
```

### 2. Navigate to the project directory

```bash
cd customer-churn-analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
churn.ipynb
```

Make sure `customer_churn.csv` is present in the same directory as the notebook.

---

# 📌 Conclusion

This project demonstrates how **Exploratory Data Analysis can be used to understand customer churn and identify potentially high-risk customer segments**.

The analysis found that churn is particularly associated with factors such as **short customer tenure, month-to-month contracts, Fiber optic internet service, lack of certain additional services, senior-citizen status, and Electronic Check payment methods**.

The findings can help businesses prioritize retention efforts, improve the early customer experience, encourage longer-term contracts, and investigate service or payment-related issues.

---

## 📚 Skills Demonstrated

- Data Loading
- Data Cleaning
- Data Type Conversion
- Missing Value Analysis
- Duplicate Detection
- Descriptive Statistics
- Exploratory Data Analysis
- Data Visualization
- Countplots
- Pie Charts
- Histograms
- Subplots
- Categorical Data Analysis
- Business Insight Generation
- Customer Churn Analysis
- Data Storytelling

---

## 👨‍💻 Author

**Aadil**

Aspiring Data Analyst | Python | SQL | Excel | Data Visualization

---

⭐ If you found this project useful, consider giving the repository a star!