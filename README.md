# Sales Performance Dashboard

I built this dashboard to analyze one full year of sales data across different regions and product categories. The goal was simple — look at the numbers and figure out where the business is doing well and where it isn't.

Everything is done in Excel. Pivot tables, charts, a dashboard — the works.

---

## Files

- `Sales_Performance_Dashboard.xlsx` — the main file, open this
- `sales_raw_data.csv` — the raw data I worked with

---

## The Data

300 rows of sales records covering January to December 2023.

Each row represents one month of sales for one region and one product category.

**Regions:** North, South, East, West, Central

**Categories:** Electronics, Clothing, Furniture, Groceries, Sports

**Columns:** Month, Region, Category, Sales, Units Sold, Profit, Profit Margin %

---

## What I Did

**Data Cleaning**
- Checked for missing values and duplicates — found none
- Made sure all region and category names were consistent
- Added a Profit Margin % column

**Pivot Tables**
- Sales and profit broken down by region
- Sales, profit, and units broken down by category
- Month-by-month sales trend with MoM growth %
- A region vs category cross table to see which combination performs best

**Charts**
- Bar chart for regional sales comparison
- Line chart for the monthly trend
- Pie chart for profit share by category

**Dashboard**
- One sheet with all the key numbers at the top — total sales, total profit, margin, units sold
- Quick view of which region and category is performing best
- All numbers pull automatically from the pivot tables so nothing needs to be updated manually

---

## What I Found

Total sales for the year came out to ₹8.14 crore with an average profit margin of 22.2%.

**South region had the highest sales** but North had the best profit margin at 23.6% — meaning North is actually more efficient even though it sells less.

**Electronics had the lowest total sales** but one of the higher margins. There's room to push volume there.

**Furniture had the worst margin** at 20.8% — worth looking into whether pricing or costs are the issue.

Sales dipped pretty noticeably from June to August across all regions. That mid-year slump is consistent enough that it's probably seasonal — promotions during that period could help.

---

## Formulas I Used

```
=SUMIF(B:B, "North", D:D)                             → total sales for one region
=SUMIFS(D:D, B:B, "North", A:A, "Jan 2023")           → sales filtered by region and month
=(B4-B3)/B3                                            → month over month growth
=INDEX(A4:A8, MATCH(MAX(B4:B8), B4:B8, 0))            → find top performing region
=AVERAGEIF(C:C, "Electronics", G:G)                   → average margin for one category
```

---

## How to Open

Download `Sales_Performance_Dashboard.xlsx` and open it 

Start on the Dashboard sheet. If you want to explore the numbers, the pivot tables are on the other sheets. The Raw Data sheet has all 300 rows.

---

**Tanish Sharma**
B.Sc. Statistics — Delhi University, PGDAV College
[LinkedIn](https://linkedin.com/in/grt-tanish) · Tanishshr1234@gmail.com
