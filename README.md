# SokoMart_Performance_and_Sales-Analytics
Enterprise Power BI suite analyzing $2.86M in revenue, customer churn exposure, and dynamic win-back projections.
# Soko Mart: Enterprise Revenue Optimization & Churn Diagnostic Analytics



## 📌 Executive Summary
Soko Mart is an e-commerce platform processing **$2.86M** in total revenue across **943 customer orders**. This project establishes an enterprise-grade Power BI reporting suite designed to monitor sales health, evaluate product category margins, identify dormant customer risk, and simulate recovery potential.

---

## 💡 Key Business Findings
* **Churn Risk Exposure**: **$497.23K (17.4% of total revenue)** is currently sitting in the **At-Risk** RFM customer tier across 29 accounts.
* **Critical Decay Band**: **$340K** of At-Risk capital sits in the **181–360 day inactivity window**, marking the primary target for re-engagement before crossing into permanent churn ($783.39K).
* **High-Margin Drivers**: **Fashion** generates the highest basket yield with an **Average Order Value (AOV) of $4,422.47**, compared to **Groceries ($597.10 AOV)**.
* **Category Baseline**: **Home** serves as the core revenue anchor, driving **$1.04M (36.5% share)** across 244 transactions.

---

## 🛠️ Dashboard Architecture

| Dashboard Page | Purpose & Core Insights |
| :--- | :--- |
| **1. Executive Overview** | High-level business performance, revenue trends, and key regional drivers. |
| **2. Customer Health & Behaviour** | RFM segmentation mapping customer lifetime value against purchase frequency. |
| **3. Product & Sales Performance** | Product category dynamics, order volume vs. AOV scatter analysis, and basket trends. |
| **4. Churn & At-Risk Diagnostic** | Interactive scenario simulator, decay band sorting, and CRM action priority matrices. |

---

## 🧮 Advanced DAX Features & What-If Simulation
The report features a dynamic **What-If Win-Back Simulator** allowing executives to test campaign recovery targets live:

```dax
Simulated Win-Back Cash = 
VAR AtRiskRevenue = CALCULATE([Total Revenue], Customers[RFM_Segment] = "At_Risk")
VAR RecoveryPercentage = 'Win-Back Recovery Rate'[Win-Back Recovery Rate Value]
RETURN
    AtRiskRevenue * RecoveryPercentage
```

---

## 📸 Dashboard Gallery

### Page 2: Customer Health & Behaviour
![Customer Health](images/02_Customer_Health.png)

### Page 3: Product & Sales Performance
![Product Performance](images/03_Product_Performance.png)

### Page 4: Churn & At-Risk Diagnostic
![Churn Diagnostic](images/04_Churn_Diagnostic.png)

---

## 🔧 Technical Stack
* **Tool**: Microsoft Power BI Desktop
* **Language**: DAX (Data Analysis Expressions)
* **Data Modeling**: Star Schema (Fact Orders, Dim Customers, Dim Products, Dim Date)
