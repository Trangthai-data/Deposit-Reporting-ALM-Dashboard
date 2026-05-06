# 📊 Deposit Reporting & Financial Dashboard (ALM Perspective)

![Dashboard Overview](images/overview-dashboard.png)

Banking analytics project focusing on deposit reporting, funding structure analysis, Cost of Fund (COF), and ALM decision support.

This project simulates an end-to-end banking reporting workflow, including data processing, financial data modeling, and dashboard analytics to support funding strategy and ALM management.

---

## 🧠 Business Problem

Banks need to control funding costs (COF) and optimize Net Interest Margin (NIM) through effective deposit structure management.

However:

- Deposit data is fragmented across:
  - CASA
  - Savings
  - Term Deposits
- Difficult to determine balances at a specific as-of date
- Lack of analytical tools for:
  - Tenor structure
  - CASA ratio
  - Funding structure impact on COF & NIM

👉 As a result:

- Funding optimization decisions become difficult
- Business impact from funding strategy changes cannot be quantified effectively

---

## 🎯 Objectives

- Build deposit dataset at as-of date
- Standardize data for financial analytics
- Monitor:
  - CASA Ratio
  - COF
  - Interest Expense
- Simulate scenarios:
  - CASA increase
  - Tenor adjustment
- Evaluate NIM impact

---

## 🏗️ Data Architecture

```text
TIENGUI_THANHTOAN
TIENGUI_TIETKIEM
TIENGUI_COKYHAN
KHACHHANG
        ↓
Stored Procedure (as-of date snapshot)
        ↓
SQL View / Function (standardization)
        ↓
Power BI Dataset (Star Schema)
        ↓
Dashboard (ALM Analytics)
```

---

## ⚙️ Technical Highlights

### SQL Server

- Built Stored Procedures for:
  - Deposit snapshot at as-of date
  - Balance aggregation by product & customer

---

### Data Standardization

- Function & View for:
  - Deposit type mapping
  - Interest rate normalization
  - Currency standardization

---

### Data Modeling

#### Star Schema

- Date
- Customer
- Product
- Fact Deposit

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

### Cost of Fund (COF)

```text
COF = Interest Expense / Average Funding Balance
```

---

### Interest Expense

```text
Interest Expense = Σ(Deposit Interest Cost)
```

---

### NIM Impact

```text
NIM Impact = Loan Yield - COF
```

---

## 💡 Insights & Decisions

### 1. CASA remains very low (~2.9%)

👉 Heavy reliance on term deposits keeps COF elevated.

#### Recommended Action

- Increase CASA by 3–5% through:
  - Transaction banking
  - Payroll products
  - Digital banking ecosystem

---

### 2. Short-term tenor (1–3M) dominates the portfolio (~57%)

👉 Main funding source but still carries meaningful funding cost.

#### Recommended Action

- Optimize pricing strategy
- Rebalance tenor allocation

---

### 3. Medium-to-long tenor deposits (6–12M) contribute heavily to interest expense

#### Recommended Action

- Limit aggressive long-term deposit growth
- Shift funding mix toward short/medium tenor

---

### 4. COF is highly sensitive to funding structure changes

👉 Funding mix should be managed as a strategic ALM lever.

---

### 5. Combined scenario (higher CASA + lower long tenor) creates strongest COF optimization

#### Recommended Action

- Execute multiple funding strategies simultaneously instead of isolated actions

---

## 🚀 Business Impact

### ⏱️ Operational Efficiency

- Reduced manual reporting & data processing time by ~50–70%

---

### 📊 Standardized ALM Dataset

- Improved data consistency for financial analysis

---

### 🧠 Better Decision Support

Supports decisions related to:

- Funding strategy
- Deposit pricing
- Liquidity management

---

## 🔍 Future Enhancements

- Connect Loan data for full NIM calculation
- Build loan product yield analytics
- COF decomposition by tenor
- Repricing gap analysis (banking ALM standard)
- Near real-time dashboard development

---

## 🧩 Technology Stack

### SQL Server

- Stored Procedure
- Function
- View
- Aggregation

---

### Power BI

- Data Modeling
- DAX
- Visualization
- Financial Dashboard

---

## ✅ Key Takeaway

The project demonstrates how banks can build an end-to-end ALM reporting system to analyze funding structure, optimize Cost of Fund, and support strategic financial decision-making.

---

## 👩‍💻 Author

**Trang Thai**

- GitHub: https://github.com/Trangthai-data
