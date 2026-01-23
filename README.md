# End To End Tableau Business Intelligence Project 

> 📊 **Interactive business intelligence dashboards built in Tableau with a strong focus on extracting business insights.**

---

## Project Overview
This project delivers an **end-to-end Tableau analytics solution** designed to support business stakeholders with clear, actionable insight.  
The work spans **requirements definition, KPI design, analytical logic, interactivity, and UX-driven dashboard layout**
---

## Project Components (Click to Explore)

Each component below links to a dedicated Markdown file explaining the **analytical approach, KPIs, and insights** behind the visuals.

- 📈 **[Sales Dashboard – Performance & Trends](sales/sales_dashboard.md)**
- 👥 **[Customer Dashboard – Behaviour & Value](customers/customer-dasboard.md)**
- 📊 **[Customer Distribution by Number of Orders](PLACEHOLDER_customer_distribution.md)**
- 🏆 **[Top Ten Customers Analysis](PLACEHOLDER_top_ten_customers.md)**
---

## Analytical Framework
All dashboards are driven by **Year-over-Year (YoY) analysis**, allowing users to dynamically select any year as the “current” year and compare performance against the previous year.

The analysis follows a consistent **Dimensions vs Measures** framework to ensure:
- Correct aggregation
- Analytical clarity
- Scalability across dashboards

---

## Live Dashboard Access

🔗 **Tableau Public (Interactive Dashboards):**  
`[PLACEHOLDER – insert Tableau Public profile or dashboard link here]`

> Dashboards can be explored interactively, including full filtering, navigation, and tooltip functionality.

---

## Dashboard Preview

### Sales Dashboard
📌 *Overview of sales performance, trends, and product contribution*

![Sales Dashboard – Full View](images/sales_dashboard_full.png)

---

### Customer Dashboard
📌 *Analysis of customer behaviour, distribution, and value contribution*

![Customer Dashboard – Full View](images/customer_dashboard_full.png)

---

## Business Objectives
This project enables stakeholders to:
- Monitor sales, profit, and volume at a glance
- Understand which products and categories drive performance
- Analyse customer behaviour and identify high-value customers
- Detect trends, seasonality, and performance anomalies

---

## Interactivity & Navigation

- **Dynamic Year Selection**
  - Any year can be treated as the “current” year
  - All KPIs and trends update automatically

- **Dashboard Navigation**
  - Icon-based navigation between analytical views
  - Active states clearly indicate the current dashboard

- **Chart-Driven Filtering**
  - Charts act as interactive filters across views
  - Customer and product selections propagate across dashboards

- **Collapsible Filter Panel**
  - Product filters: Category, Subcategory
  - Location filters: Region, State, City
  - Toggleable container preserves screen space

![Filters Panel](images/filters_panel.png)

---

## Data Architecture & Model

- **Model Type:** Star Schema (implemented using Tableau Relationships)
- **Fact Table:** Orders
- **Dimension Tables:** Customers, Products, Locations
- **Keys:** Unique IDs linking fact and dimensions

![Data Model](images/data_model.png)

---

## Technical Highlights

- Parameters for dynamic year selection
- Window functions for automatic Min/Max detection
- LOD expressions for customer order-frequency analysis
- Reference lines for weekly averages
- Custom tooltips for enhanced interpretability

---

## Tools Used
- Tableau Desktop / Tableau Public
- CSV Flat Files
- Custom icons for navigation and filters

---

## How to Use
1. Select a year using the **Year Parameter**
2. Navigate analytical views via the **icon buttons**
3. Open the **filter panel** to refine results
4. Click charts and tables to apply cross-filtering
