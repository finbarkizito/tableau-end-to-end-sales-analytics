# Tableau Sales & Customer Analytics Dashboard

> 📊 **Interactive business intelligence dashboards built in Tableau with a strong focus on analytical design, interactivity, and user experience.**

---

## Project Overview
This project delivers an **end-to-end Tableau analytics solution** developed to support business stakeholders with clear, actionable insight. The work spans **requirements definition, KPI design, analytical logic, interactivity, and UX-driven dashboard layout**, ensuring the final output is decision-ready and scalable.

The solution consists of two integrated dashboards:
- **Sales Dashboard**
- **Customer Dashboard**

Both dashboards are driven by **Year-over-Year (YoY) analysis**, allowing users to dynamically select any year as the “current” year and compare performance against the previous year.

---

## Live Dashboard Access

🔗 **Tableau Public (Interactive Dashboards):**  
`[PLACEHOLDER – insert Tableau Public profile or dashboard link here]`

> The dashboards can be explored interactively via Tableau Public, including full filtering, navigation, and tooltip functionality.

---

## Dashboard Preview

### Sales Dashboard
📌 *Overview of sales performance, trends, and product contribution*

<!-- IMAGE PLACEHOLDER: Sales Dashboard (Full View) -->
![Sales Dashboard – Full View](images/sales_dashboard_full.png)

---

### Customer Dashboard
📌 *Analysis of customer behaviour, distribution, and value contribution*

<!-- IMAGE PLACEHOLDER: Customer Dashboard (Full View) -->
![Customer Dashboard – Full View](images/customer_dashboard_full.png)

---

## Business Objective
The objective of this project is to enable stakeholders to:
- Monitor sales, profit, and volume at a glance
- Understand which products and categories drive revenue
- Analyse customer behaviour and identify high-value customers

All analysis follows a **Dimensions vs Measures** framework to ensure clarity, consistency, and scalability.

---

## Sales Dashboard – Key Features

### KPI Overview (BANs)
- Total Sales
- Total Profit
- Total Quantity  

Each KPI displays:
- Current year value
- Previous year comparison
- Directional indicators (▲ / ▼)

<!-- IMAGE PLACEHOLDER: KPI BANs -->
![Sales KPIs](images/sales_kpis.png)

---

### Monthly Trends (Sparklines)
- Monthly Sales, Profit, and Quantity
- Current vs Previous year comparison
- Automatic highlighting of highest and lowest months

<!-- IMAGE PLACEHOLDER: Monthly Sparklines -->
![Monthly Trends](images/sales_sparklines.png)

---

### Product Subcategory Analysis
- **Bar-in-Bar charts** for YoY Sales comparison
- **Side-by-side bar charts** for Profit analysis

<!-- IMAGE PLACEHOLDER: Subcategory Comparison -->
![Subcategory Analysis](images/subcategory_analysis.png)

---

### Weekly Performance Trends
- Weekly Sales and Profit
- Dynamic average reference line
- Visual distinction between above- and below-average weeks

<!-- IMAGE PLACEHOLDER: Weekly Trends -->
![Weekly Trends](images/weekly_trends.png)

---

## Customer Dashboard – Key Features

### Customer KPI Overview
- Total Customers
- Sales per Customer
- Total Orders
- YoY comparison included

<!-- IMAGE PLACEHOLDER: Customer KPIs -->
![Customer KPIs](images/customer_kpis.png)

---

### Monthly Customer Trends
- Monthly performance trends
- Highlighted peaks and troughs

<!-- IMAGE PLACEHOLDER: Customer Sparklines -->
![Customer Trends](images/customer_sparklines.png)

---

### Customer Distribution
- Histogram showing customers grouped by number of orders
- Built using **Level of Detail (LOD) expressions**

<!-- IMAGE PLACEHOLDER: Customer Distribution Histogram -->
![Customer Distribution](images/customer_distribution.png)

---

### Top 10 Customers
- Ranked by Profit
- Includes:
  - Rank
  - Number of Orders
  - Current Sales
  - Current Profit
  - Last Order Date

<!-- IMAGE PLACEHOLDER: Top Customers Table -->
![Top Customers](images/top_customers.png)

---

## Interactivity & Navigation

- **Dynamic Year Selection**
  - Users can select any year as the “current” year
  - All visuals update automatically

- **Dashboard Navigation**
  - Icon-based navigation between Sales and Customer dashboards
  - Active/inactive states indicate current view

- **Chart-Driven Filtering**
  - Charts act as interactive filters
  - Histogram and Top Customers table drive cross-filtering

- **Collapsible Filter Panel**
  - Product filters: Category, Subcategory
  - Location filters: Region, State, City
  - Toggleable container to preserve screen space

<!-- IMAGE PLACEHOLDER: Filter Panel -->
![Filters Panel](images/filters_panel.png)

---

## Design & UX Principles

- Consistent layout across dashboards
- Limited colour palette:
  - Two neutral greys
  - Two accent colours for emphasis
- Clean spacing and alignment using containers
- Custom tooltips for improved readability

---

## Data Architecture & Model

- **Model Type:** Star Schema (implemented via Tableau Relationships)
- **Fact Table:** Orders
- **Dimension Tables:** Customers, Products, Locations
- **Keys:** Unique IDs linking fact and dimensions

<!-- IMAGE PLACEHOLDER: Data Model -->
![Data Model](images/data_model.png)

---

## Technical Highlights

- **Parameters:** Dynamic year selection
- **LOD Expressions:** Customer order frequency analysis
- **Window Functions:** Automatic Min/Max detection
- **Reference Lines:** Dynamic weekly averages
- **Custom Tooltips:** Fully redesigned tooltips

---

## Insights & Observations
📌 *Placeholder for analytical findings derived from the dashboards.*

Examples:
- Key revenue-driving categories and subcategories
- Seasonal sales patterns and weekly performance behaviour
- Customer segments contributing disproportionate profit
- Differences between high-volume and high-value customers

`[PLACEHOLDER – insert insights once analysis is finalised]`

---

## Tools Used
- Tableau Desktop / Tableau Public
- CSV Flat Files
- Custom Icons for navigation and filters

---

## How to Use
1. Select a year using the **Year Parameter**
2. Navigate dashboards via the **icon buttons**
3. Open the **filter panel** to refine results
4. Click charts and tables to apply interactive filters
