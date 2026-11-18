# TechMart Sales & Customer Segmentation Dashboard

An interactive, single-file analytics dashboard (HTML + JavaScript + Chart.js) for a fictional Saudi e-commerce store. It covers the full analysis flow: **raw data → cleaning → KPIs → exploratory charts → RFM customer segmentation → marketing recommendations**.

> **Note:** the dataset is synthetic. It is generated deterministically in the code (fixed seed), so the numbers below are reproducible.

## Live Demo
Open `index.html` in any browser, or host it on GitHub Pages (Settings → Pages → deploy from the `main` branch).

## Features
- **Data cleaning pipeline** – a simulated raw table (1,125 rows) is cleaned to 1,100 rows: 25 duplicate orders removed, 30 missing cities imputed from the customer record, 35 city names trimmed, and 8 outlier quantities (> 10) replaced with the median. A "Data quality" panel reports each step.
- **KPIs with period comparison** – total sales, orders, average order value, and active customers, with month-over-month change.
- **Interactive filters** – city, category, date range, and free-text search. Every KPI, chart, and table updates instantly. Clicking a bar in the category or city chart also filters.
- **Charts** – monthly sales trend, sales by category, sales by city, RFM segment distribution.
- **RFM segmentation (quintiles)** – Recency, Frequency, and Monetary scores from 1 to 5, five segments, and a recommended marketing action per segment.
- **Top customers** and a **sortable, paginated orders table**.
- **CSV export** of the filtered orders.
- Responsive layout, light/dark mode, right-to-left Arabic interface.

## Key Insights (full dataset)
| Metric | Value |
|---|---|
| Total sales | 471,160 SAR |
| Orders | 1,100 |
| Average order value | 428 SAR |
| Top category | Electronics: 43.2% of sales |
| Top city | Riyadh: 34.3% of sales |
| Weakest city | Tabuk: 6.6% of sales |
| Sales growth | October sales were about 22% higher than September (74,090 vs 60,840 SAR) |

Findings worth acting on:
1. **Electronics drives almost half of revenue.** Stock and promotion decisions should start there.
2. **Riyadh alone generates over a third of sales.** Growth in Jeddah and the western region is the biggest untapped opportunity.
3. **Sales grew steadily through the year**, from about 12k SAR in January to 74k SAR in October.

## RFM Segments
| Segment | Rule | Suggested action |
|---|---|---|
| Champions | R ≥ 4, F ≥ 4, M ≥ 3 | Loyalty rewards; early access to new products |
| Loyal | R ≥ 3, F ≥ 3 | Upsell and points programs |
| New | R ≥ 4 | Welcome message and second-order offer |
| At risk | R ≤ 2, F ≥ 3 | Time-limited win-back discount |
| Sleeping | Everything else | Low-cost reminders; no paid ads |

## Tech Stack
HTML5 · CSS3 · Vanilla JavaScript · [Chart.js](https://www.chartjs.org/) 4.4

## Project Structure
```
├── index.html   # the whole dashboard (data, cleaning, analysis, UI)
└── README.md
```

## Limitations & Next Steps
- Replace the synthetic data with a real open dataset (for example, an e-commerce dataset from Kaggle) and adapt the cleaning step.
- Add a Python notebook that reproduces the cleaning and RFM analysis with pandas.
- Add a PDF report export.

## Author
**Your Name** · [LinkedIn](https://linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)
