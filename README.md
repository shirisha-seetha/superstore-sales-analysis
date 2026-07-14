# Superstore Sales Analysis

End-to-end sales analysis of the Sample Superstore dataset, built across three tools — *Excel, **Power BI, and **Python (Pandas)* — to explore regional performance, category profitability, discount impact, and customer behavior.

---

## Dataset Overview

| Metric | Value |
|---|---|
| Total Records | 9,354 |
| Total Orders (distinct) | 6,428 |
| Total Sales | $87,89,581.77 |
| Total Profit | $12,80,490.84 |
| Profit Margin | 14.57% |
| Average Sale | $40,975.80 |
| Max / Min Sale | $1,00,119.16 / $1.32 |
| Max / Min Profit | $16,332.41 / -$16,476.84 |

*Dimensions covered:* Region (Central, East, South, West) · Category (Furniture, Office Supplies, Technology) · Customer Segment (Consumer, Corporate, Home Office, Small Business) · Ship Mode · Order Date · Discount Level

---

## Tools Used

| Tool | What it covers |
|---|---|
| *Excel* | PivotTables, PivotCharts, slicers, KPI cards — a full interactive dashboard (EDA tab for detailed breakdowns, Overview tab as the dashboard) |
| *Power BI* | Two-page report — Sales Dashboard (KPIs, regional/category trends, discount analysis, top customers) and Product Performance Analysis (top/bottom products, customer segment mix) |
| *Pandas (Python)* | Data cleaning, statistical analysis (correlation, significance testing, outlier detection), RFM customer segmentation, and visualizations |

---

## Key Insights

1. *Discounting hurts profit* — profit drops sharply once discount crosses roughly 5–6%, and turns negative beyond ~8–9%. The relationship is statistically significant (see Pandas notebook, Section 5).
2. *Furniture generates strong sales but thin margins* compared to Technology, which delivers the best profit-to-sales ratio of the three categories.
3. *Central and West regions lead in total sales*, but profit margins vary more than sales do — South lags noticeably in profit despite reasonable sales volume.
4. *A small share of customers drive a disproportionate share of profit* — consistent with a Pareto-style pattern (see RFM segmentation in the Pandas notebook).
5. *Certain sub-categories are consistent loss-makers* (e.g., Tables, Bookcases) even though they contribute meaningfully to total sales — a classic Superstore-dataset finding.
6. Monthly sales/profit show clear *seasonality*, peaking toward Q4 (Nov/Dec).

---

## Screenshots

### Excel Dashboard
![Excel Overview](screenshots/excel_overview.png)

### Excel EDA Sheet
![Excel EDA](screenshots/excel_eda.png)

### Power BI — Sales Dashboard
![Power BI Page 1](screenshots/powerbi_page1.png)

### Power BI — Product Performance Analysis
![Power BI Page 2](screenshots/powerbi_page2.png)

### Discount vs Profit (Pandas)
![Discount vs Profit](screenshots/discount_vs_profit.png)

---

## Project Structure

```
superstore-sales-analysis/
├── README.md
├── data/
│   └── SampleSuperstore.csv
├── excel/
│   └── superstore_dashboard.xlsx
├── powerbi/
│   └── superstore_dashboard.pbix
├── pandas/
│   └── superstore_analysis.ipynb
└── screenshots/
    ├── excel_overview.png
    ├── excel_eda.png
    ├── powerbi_page1.png
    ├── powerbi_page2.png
    └── discount_vs_profit.png
```

---

## How to Use

*Excel:* Open excel/superstore_dashboard.xlsx — use the slicers on the Overview tab to filter by Region, Category, Segment, Ship Mode, or Order Date. The EDA tab contains the full set of underlying pivot tables.

*Power BI:* Open powerbi/superstore_dashboard.pbix in Power BI Desktop (free). Page 1 is the main dashboard; Page 2 covers product-level performance.

*Pandas:* Open pandas/superstore_analysis.ipynb in Jupyter. Update the FILE_PATH variable to point to data/SampleSuperstore.csv, then run all cells.

---

## Data Source

Sample Superstore dataset — a widely used sample retail dataset (orders, customers, products, sales, and profit across the US), commonly used for BI/analytics practice.