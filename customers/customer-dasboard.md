# Customer Analytics Dashboard  
**Segmentation & Behaviour Analysis**

---

## 1. Business Problem & Objectives
While the Sales Dashboard focuses on *what* was sold, the **Customer Dashboard** focuses on *who* is buying.  
The objective is to analyse customer behaviour, retention, and profitability to support targeted commercial and marketing decisions.

Key business questions addressed include:
- Are we growing or losing active customers year-over-year?
- How frequently do customers place orders?
- Who are the most profitable customers, and how recently have they purchased?
- Is revenue per customer increasing or declining?

---

## 2. Key Performance Indicators (KPIs) & Metrics
The dashboard tracks customer health using **Current Year vs Previous Year** comparisons.

| KPI / Metric | Logic & Calculation | Analytical Purpose |
|--------------|--------------------|-------------------|
| **Total Customers** | `COUNTD([Customer ID])` filtered by `YEAR([Order Date]) = [Select Year]` | Measures the size of the active customer base |
| **Sales per Customer (ARPU)** | `Current Year Sales / COUNTD(Current Year Customers)` | Indicates customer value and spending behaviour |
| **Total Orders** | `COUNTD([Order ID])` for the selected year | Reflects transaction volume and operational load |
| **Customer Rank** | `RANK_DENSE(SUM([Profit]))` | Identifies top contributors to profitability |

---

## 3. Data Preparation & Advanced Transformations
The analysis relies on **Level of Detail (LOD)** expressions and parameter-driven logic to transform transactional data into customer-level insights.

### Customer Order Frequency (LOD)
To analyse purchase behaviour, the number of orders per customer was calculated before aggregation.

```text
{ FIXED [Customer Name] : COUNTD([Order ID]) }

