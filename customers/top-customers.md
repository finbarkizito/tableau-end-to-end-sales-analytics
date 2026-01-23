# 🏆 Top Ten Customers Analysis  
**Profitability, Recency & Contribution**

---

## 1. Business Problem & Objective
While aggregate metrics describe overall performance, decision-making often depends on understanding **who drives profit** at the individual customer level.  
This analysis isolates the **Top 10 customers by profit** to support retention, account management, and margin protection.

Key questions addressed:
- Which customers contribute most to total profit in the selected year?
- When did these high-value customers last place an order?
- Is profitability driven by frequent purchasing or high-value transactions?

---

## 2. Key Metrics & KPIs
The table combines financial and behavioural metrics to create a complete **VIP customer profile**.

| Metric | Calculation / Logic | Analytical Purpose |
|-------|---------------------|-------------------|
| **Rank** | `INDEX()` table calculation | Establishes a clear profit-based hierarchy (1–10) |
| **Current Year Profit** | `SUM([Current Year Profit])` | Identifies true bottom-line contributors |
| **Last Order Date** | `MAX([Order Date])` | Flags recency risk among high-value customers |
| **Order Count** | `COUNTD([Order ID])` (Current Year) | Distinguishes frequency-driven vs value-driven profit |
| **Current Year Sales** | `SUM([Current Year Sales])` | Provides revenue context relative to profit |

---

## 3. Data Preparation & Logic
Specific filtering and aggregation logic was applied to ensure the ranking is dynamic and accurate.

- **Top N Filtering**
  - Implemented using a Set / Filter on `[Customer Name]`
  - Configured to select the **Top 10 by Sum of Profit**
  - Automatically updates as data or year selection changes

- **Time Context**
  - All calculations reference the shared `Select Year` parameter
  - Prevents historical profit from influencing current-year rankings

- **Table Calculations**
  - `INDEX()` converted to discrete to display rank as a column header
  - Sorting enforced on Profit to maintain ranking integrity

---

## 4. Visual Design & UX
The visual is intentionally designed as a **Symbol Table** rather than a default Tableau text table.

- **Custom Headers**
  - Default headers hidden
  - Replaced with text objects in a horizontal container for precise alignment

- **Visual Hierarchy**
  - Rank visually separated using a light background and prefix (`#1`, `#2`, etc.)
  - Profit column dynamically labelled using the selected year (e.g. *2023 Profit*)

- **Minimalist Layout**
  - Gridlines and row banding removed
  - Emphasis placed on values, not table structure

---

## 5. Analytical Interactivity
The table acts as a **primary drill-down control** for the dashboard.

- **Chart-as-Filter**
  - Selecting a customer filters:
    - KPIs
    - Monthly sparklines
    - Supporting distribution views
- **Insight Generation**
  - Reveals whether a customer’s rank is driven by:
    - Consistent purchasing behaviour
    - A single high-value transaction
    - Seasonal spikes

---

## 6. Stakeholder Usage
**How an Account Manager uses this analysis:**

1. Reviews the Top 10 list to prioritise outreach
2. Scans **Last Order Date** to identify dormant VIPs
3. Clicks a customer to assess buying patterns and seasonality
4. Compares **Sales vs Profit** to detect margin erosion from discounts

This visual supports targeted retention, proactive account management, and profit optimisation.

