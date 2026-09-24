# TeleConnect — Customer Churn Analysis

## 📌 Project Overview

**TeleConnect Customer Churn Analysis** is a data analysis project focused on understanding customer churn and identifying customer profiles associated with higher churn.

The main objective is to answer:

> **Who is leaving, and what do they have in common?**

The analysis uses data cleaning, exploratory data analysis, visualization, and statistical testing to identify important patterns in customer churn.

---

## 🎯 Objectives

* Clean and validate a customer dataset.
* Calculate the overall customer churn rate.
* Analyze churn across contract types, plans, cities, and tenure.
* Compare support-call behavior between churners and stayers.
* Identify high-risk customer segments.
* Perform statistical hypothesis testing.
* Analyze monthly charges within different plan types.
* Provide data-driven insights for customer retention.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — Data cleaning and analysis
* **NumPy** — Numerical operations
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **SciPy** — Statistical hypothesis testing
* **Jupyter Notebook**

---

## 📊 Dataset

The dataset contains approximately 7,000 customer records with information including:

* Customer ID
* City
* Age
* Gender
* Tenure
* Plan Type
* Contract Type
* Monthly Charges
* Total Charges
* Support Calls
* Payment Method
* Broadband Subscription
* Streaming Subscription
* Churn Status

The original dataset contains deliberately messy values that require preprocessing before analysis.

---

## 🧹 Data Cleaning

The following data-quality issues were addressed:

* Duplicate customer records
* Inconsistent churn values such as `Yes`, `yes`, `No`, `no`, `1`, and `0`
* Currency symbols and commas in monthly charges
* Tenure values represented in both months and years
* Invalid age values
* Inconsistent city capitalization
* Missing total charges

After cleaning, the dataset contains **6,996 customers and 14 columns**.

---

## 🔍 Key Findings

### Overall Churn

The overall customer churn rate is approximately:

**22.21%**

### Contract Type

Month-to-month customers have a churn rate of approximately **35.65%**, while two-year customers have a churn rate of approximately **3.91%**.

A chi-square test found a statistically significant association between contract type and churn:

**χ² = 876.66, p < 0.001**

### Support Calls

Churners averaged approximately **1.58 support calls**, compared with **1.11** for customers who stayed.

Welch's t-test showed a statistically significant difference:

**p < 0.001**

The effect size was:

**Cohen's d = 0.432**

This indicates a moderate difference, but the analysis does not establish that support calls cause churn.

### High-Risk Customer Profile

A particularly high-risk profile was identified as:

* Month-to-month contract
* Tenure ≤ 6 months
* 2 or more support calls

This segment contains **213 customers** and has a churn rate of approximately **62.44%**, including **133 churners**.

### Monthly Charges

Within the Basic and Premium plans, churners had statistically lower average monthly charges than stayers. For the Standard plan, the difference was not statistically significant.

This analysis therefore does not support the conclusion that higher monthly charges are associated with higher churn within a plan.

---

## 📈 Statistical Methods

The project uses:

* **Welch's independent-samples t-test**
* **Cohen's d effect size**
* **Chi-square test of independence**
* Contingency tables
* Group-level descriptive statistics

The analysis focuses on **association rather than causation**.

---

## 💡 Business Insight

The analysis suggests that retention efforts should pay particular attention to customers with **month-to-month contracts**, especially newer customers who have made multiple support calls.

The high-risk profile can help identify a focused group for retention analysis, while the broader month-to-month customer population should also be considered because of its substantially higher observed churn rate.

---

## ⚠️ Project Scope

This project focuses on **customer churn analysis, exploratory data analysis, visualization, and statistical inference**.

The project does not build machine-learning prediction models. The findings represent associations observed in the available customer data and should not be interpreted as proof of causation.

---

## 👨‍💻 Author

**Thrishul Sri Chandra Arala**

Data Science | Python | Machine Learning | Generative AI
