# 📈 Sales Performance Dashboard  
**Analytical Approach & Technical Implementation**

---

## 📊 Dashboard Preview

[Dashboard Preview](/images/sales_dashboard.png)

<!-- DASHBOARD IMAGE PLACEHOLDER -->
<!-- Replace the line below with: ![Dashboard Preview](path/to/image.png) -->

---
## 1. Business Problem & Objectives
The goal of this dashboard is to enable stakeholders to analyse **Year-over-Year (YoY) sales performance** in a dynamic and interactive way. The dashboard supports:

- Monitoring overall sales growth or decline versus the prior year  
- Identifying seasonal patterns and monthly fluctuations  
- Isolating products and subcategories driving profit or loss  
- Detecting weekly performance anomalies relative to an annual baseline  

Rather than static reporting, the focus is on exploratory analysis and decision support.

---

## 2. Key Performance Indicators (KPIs) & Metrics
The dashboard centres on three core measures: **Sales, Profit, and Quantity**, analysed using the following KPIs.

| KPI / Metric | Logic & Calculation | Analytical Purpose |
|--------------|--------------------|-------------------|
| **YoY Growth %** | `(Current Year Sales − Previous Year Sales) / Previous Year Sales` | Measures the rate of growth or decline relative to the prior year |
| **Current vs Previous Year Sales** | `IF YEAR([Order Date]) = [Select Year] THEN [Sales] END` and `[Select Year] - 1` | Enables direct like-for-like comparison across years |
| **Min / Max Monthly Sales** | `IF SUM([Sales]) = WINDOW_MAX(SUM([Sales]))` (and `WINDOW_MIN`) | Automatically identifies peak and low sales months |
| **Above / Below Average** | `IF SUM([Sales]) > WINDOW_AVG(SUM([Sales])) THEN 'Above' ELSE 'Below' END` | Flags weekly performance relative to the annual average |

---

## 3. Data Preparation & Transformation
To support accurate analysis, the following steps were applied within Tableau:

- **Data Modelling:**  
  A star-schema-style model was created, with **Orders** as the fact table linked to **Customers, Products, and Locations** as dimensions.

- **Dynamic Date Logic:**  
  - A parameter (`Select Year`) was introduced to avoid hard-coding a single analysis year.  
  - All YoY calculations reference this parameter, allowing any year to be treated as the “current” year.

- **Data Validation:**  
  - Ensured correct data types for dates and numeric fields  
  - Confirmed measures aggregated as continuous fields to avoid mis-aggregation

- **Granularity Control:**  
  Aggregations were handled at both **monthly** and **weekly** levels while preserving correct annual totals.

---

## 4. Dashboard Design & Interactivity

### Visual Structure
- **BANs (Big Numbers):**  
  Headline KPIs for Sales, Profit, and Quantity with directional YoY indicators.
- **Monthly Sparklines:**  
  Trend lines with automatically highlighted **minimum and maximum** months.
- **Subcategory Comparison:**  
  Bar-in-bar charts comparing Current Year vs Previous Year sales at subcategory level.

### Interactivity
- **Parameter-Driven Analysis:**  
  The `Select Year` parameter converts the dashboard from static reporting into a historical comparison tool.
- **Cross-Filtering:**  
  Clicking a subcategory filters all supporting views, isolating that product’s performance.
- **Collapsible Filters:**  
  High-cardinality filters (Region, State, City) are hidden in a collapsible container to preserve analytical focus.

---

## 5. Key Insights & Findings
Using 2023 as the selected year, the dashboard reveals:

- **Seasonality:**  
  November consistently appears as a peak sales month, while February tends to underperform.
- **Subcategory Risk Flags:**  
  Visual indicators highlight subcategories where current-year sales trail the prior year.
- **Profit vs Revenue Disconnect:**  
  Some high-revenue categories generate negative profit, signalling pricing or cost issues.
- **Weekly Volatility:**  
  Specific weeks fall materially below the annual average, indicating operational or demand-side disruption.

---

## 6. Stakeholder Usage
A Sales Manager can use the dashboard to:

1. Perform a rapid YoY health check using headline KPIs  
2. Identify seasonal highs and lows via monthly trends  
3. Spot declining or unprofitable subcategories instantly  
4. Drill into weekly performance to understand when and where issues occurred  

This workflow supports faster diagnosis and more targeted decision-making.
