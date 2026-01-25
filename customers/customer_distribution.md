# Customer Distribution by Number of Orders  
**Analytical Deep Dive: Purchase Frequency & Retention**

---

## 1. Business Problem & Objective
While total revenue is important, understanding **purchase frequency** is critical for assessing customer loyalty and retention.  
This analysis moves beyond aggregate sales to answer key behavioural questions:

- What proportion of customers are one-time buyers versus repeat purchasers?
- Can customers be segmented by exact order counts for targeted campaigns?
- Is performance driven by a large base of low-frequency buyers or a smaller group of loyal customers?

---

## 2. Technical Implementation: Level of Detail (LOD) Expressions
To analyse order frequency per customer, **FIXED Level of Detail (LOD)** expressions were required.  
Standard aggregations were insufficient because the data needed to be grouped **by customer first**, before analysing distribution.

### Analytical Logic
1. **Granularity Shift:**  
   Orders are first counted at the **customer level**, then customers are grouped by order count.
2. **Time Context:**  
   All calculations respect the dynamic `Select Year` parameter to avoid historical data contaminating the current-year analysis.

### Core Calculation
A calculated field was created to derive order frequency per customer:

```tableau
{ FIXED [Customer Name] : COUNTD([Current Year Orders]) }
