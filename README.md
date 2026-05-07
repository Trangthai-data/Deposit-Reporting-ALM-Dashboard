# 📊 Banking Deposit Reporting & Automation

![Dashboard](images/DASHBOARD%20ALM.jpg)

Banking analytics project focused on deposit reporting automation, funding structure monitoring, and ALM reporting using SQL Server and Power BI.

This project simulates an end-to-end banking reporting workflow, including data processing, reporting automation, data modeling, and dashboard development to support deposit monitoring and funding structure analysis.

---

## 🧠 Business Problem

Banks require centralized reporting systems to monitor deposit balances and funding structure at the reporting date (as-of date).

However:

- Deposit data is fragmented across multiple sources:
  - CASA
  - Savings
  - Term Deposits
- Difficult to generate accurate balance snapshots at reporting date
- Lack of standardized reporting and automation workflow
- Limited visibility into funding structure and deposit trends

👉 As a result:

- Manual reporting processes become time-consuming
- Reporting consistency is reduced
- Funding structure monitoring becomes inefficient

---

## 🎯 Objectives

- Build deposit reporting dataset at as-of date
- Standardize deposit data for reporting and monitoring
- Track:
  - Deposit Balance
  - CASA Ratio
  - Interest Expense
  - Funding Structure by tenor
- Automate deposit reporting workflow
- Support ALM monitoring through reporting dashboard

---

## 🏗️ Data Architecture

```text
TIENGUI_THANHTOAN
TIENGUI_TIETKIEM
TIENGUI_COKYHAN
KHACHHANG
        ↓
Stored Procedure (As-of-date Snapshot)
        ↓
SQL View / Function (Data Standardization)
        ↓
Power BI Dataset (Star Schema)
        ↓
Dashboard (Deposit Monitoring & Reporting)
```

---

## ⚙️ Technical Highlights

### SQL Server

- Developed Stored Procedures for:
  - Deposit snapshot generation at reporting date
  - Balance aggregation by customer and deposit type
  - Deposit reporting consolidation

---

### SQL Techniques

- CTE
- Window Function
- Aggregation
- Conditional Mapping

---

### Data Standardization

- Built SQL Views and Functions for:
  - Deposit type mapping
  - Interest rate normalization
  - Currency standardization

---

### Data Modeling

#### Star Schema

- Dim Date
- Dim Customer
- Dim Product
- Fact Deposit

---

### Power BI Development

- DAX Measures
- Interactive Dashboard
- Deposit Monitoring
- Funding Structure Analysis

---

### Data Validation

- Reconciled total balances against source systems

---

### Data Scope

- Snapshot-based reporting at as-of date
- Early withdrawal behavior is not included

---

## 📊 Core Metrics

### Total Deposit

```text
Total Deposit = Total Funding Balance
```

---

### CASA Ratio

```text
CASA Ratio = CASA Balance / Total Deposit
```

---

### Interest Expense

```text
Interest Expense = Σ(Deposit Interest Cost)
```

---

### Funding Structure

```text
Funding Structure = Deposit Distribution by Tenor & Product Type
```

---

## 💡 Key Insights

### 1. CASA ratio remained relatively low (~2.9%)

👉 The funding structure relied heavily on term deposits.

---

### 2. Short-term tenor (1–3M) accounted for the largest funding proportion (~57%)

👉 Deposit structure was concentrated in short-term funding products.

---

### 3. Medium and long-term deposits (6–12M) contributed significantly to interest expense

👉 Higher interest rates increased overall funding cost exposure.

---

### 4. Funding structure changed significantly across tenor groups and deposit products

👉 Monitoring deposit mix was important for reporting and funding analysis.

---

### 5. Dashboard improved visibility into deposit trends and reporting metrics

👉 Enabled faster monitoring of funding structure at reporting date.

---

## 🚀 Business Impact

### ⏱️ Operational Efficiency

- Reduced manual reporting and data consolidation effort by ~50–70%

---

### 📊 Standardized Reporting Dataset

- Improved data consistency for reporting and monitoring purposes

---

### 🧠 Better Monitoring Capability

- Increased visibility into:
  - Deposit structure
  - CASA ratio
  - Funding trends
  - Interest expense

---

### 📈 Reporting Support

- Supported reporting and monitoring activities for ALM analysis

---

## 🔍 Future Enhancements

- Integrate loan data for full balance sheet reporting
- Build NIM and yield monitoring
- Develop COF decomposition analysis
- Expand near real-time reporting workflow
- Enhance reporting automation process

---

## 🧩 Technology Stack

### SQL Server

- Stored Procedure
- Function
- View
- Aggregation
- CTE
- Window Function

---

### Power BI

- Data Modeling
- DAX
- Visualization
- Interactive Dashboard

---

## ✅ Key Takeaway

This project demonstrates how banks can build an end-to-end deposit reporting system using SQL Server and Power BI to automate reporting workflows, standardize deposit data, and support funding structure monitoring for ALM reporting.

---

## 👩‍💻 Author

**Trang Thai**

- GitHub: https://github.com/Trangthai-data
