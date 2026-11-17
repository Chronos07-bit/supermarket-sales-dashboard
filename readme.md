# Supermarket Sales Analysis Dashboard

Interactive management dashboard analysing supermarket sales across product categories and outlets. Built by Arka Bhattacharya for the Sapphire IQ Data Analytics project.

**Live dashboard:** `https://chronos07-bit.github.io/supermarket-sales-dashboard/`

Two versions of the same analysis are included:
- `index.html` – interactive web dashboard (HTML, CSS, JavaScript, Chart.js). Data is embedded, no server needed.
- `Supermarket_Sales_Analysis_Dashboard.xlsx` – Excel dashboard with dropdown filters, formulas and charts (sheets: Dashboard, Analysis, Statistics, Data, Notes).

## Objectives covered
| Objective | Questions answered |
|---|---|
| 1. Overall sales performance | Total sales, average sales per record, average item visibility |
| 2. Category and sales comparison | Top 4 categories vs the rest, highest and lowest categories, sales by outlet type |
| 3. Outlet performance and relationships | Low Fat vs Regular sales by outlet, visibility vs sales, category contribution by outlet type |
| 4. Statistical analysis | Mean, median, min, max, variation, outliers, average sales by category, outlet type and location |

## Key findings (all 8,523 records)
- Total sales 1,201,681; average 140.99 per record; average visibility 0.0661 (0.0705 excluding zeros).
- Top 4 categories (Fruits and Vegetables, Snack Foods, Household, Frozen Foods) = 50.6% of sales. Seafood is the lowest category.
- Supermarket Type1 earns 65.5% of sales, mainly because it has the most records; average sales per record are almost equal across outlet types.
- Visibility and sales are essentially uncorrelated (r = -0.001).
- Median 143.0, standard deviation 62.3. The IQR rule finds no outliers; 14 records are more than 2 standard deviations above the mean.

## Data preparation
- Fat content cleaned from 5 labels (Low Fat, low fat, LF, Regular, reg) to 2.
- 1,463 records have no item weight (left blank, not needed).
- 526 records have zero visibility (treated as likely missing; reported with and without them).
- Outlet size is inconsistent for three outlets, so it was not used.
- `data/supermarket_sales_clean.csv` holds the cleaned data.

## How to use
Open `index.html` in a browser (internet needed for the Chart.js script), or open the live link. Use the Outlet type, Location type and Fat content dropdowns; every KPI, chart, table and insight updates. In Excel, use the yellow dropdowns on the Dashboard sheet.

## Publish on GitHub Pages
Settings → Pages → Deploy from a branch → `main` / `(root)` → Save. The file must be named exactly `index.html` at the top level of the repo.
