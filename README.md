# SP-115 Power BI Blue — Real Estate Sales Performance Dashboard

**CS 4850 | Section 02 | Spring 2026**
**Kennesaw State University | Instructor: Sharon Perry**

Katherine Nguyen | Zakkary Byrd

---

## About

An interactive 4-page Power BI dashboard analyzing Connecticut real estate sales data from 2001–2022. The dashboard allows users to explore over 1 million transactions by town, property type, and time period using slicers, KPI cards, charts, and an interactive map of Connecticut.

---

## Dashboard Pages

- **Overview** — Total sales KPIs, sale amount by year, sale amount by property type, and a Connecticut town map
- **Property Analysis** — Transaction counts, average sale amount, and average assessed value broken down by property type
- **Regional Analysis** — Map and bar charts showing top towns by sale amount and average price
- **Time Analysis** — Year-over-year growth, monthly sale amount trends, and transaction count over time

---

## Dataset

The dataset is not included in this repository due to its size (~1.1 million records).

**Download it here before running the dashboard:**
[Connecticut Real Estate Sales 2001–2022 — Kaggle](https://www.kaggle.com/datasets/irakozekelly/connecticut-real-estate-sales-data-2001-2022-gl?resource=download)

After downloading, place the CSV file in a location of your choice and update the file path in Power Query inside the `.pbix` file to match.

---

## How to Run

1. Install **Microsoft Power BI Desktop** (Windows only) — [Download here](https://powerbi.microsoft.com/en-us/desktop/)
2. Download the dataset from the Kaggle link above
3. Open `SP115-Blue-PBISales.pbix` in Power BI Desktop
4. Go to **Home → Transform Data → Data Source Settings** and update the CSV file path to where you saved the dataset
5. Click **Close & Apply**, then click **Refresh** to load the data
6. All four dashboard pages will populate automatically

---

## Tools & Technologies

- Microsoft Power BI Desktop
- Power Query (data import and cleaning)
- DAX (calculated measures)
- Connecticut Real Estate Sales dataset (data.ct.gov via Kaggle)
- GitHub (version control)

---

## Key DAX Measures

- `Total Sale Amount` — sum of all sale amounts
- `Average Sale Amount` — average sale amount per transaction
- `Sales Ratio` — assessed value divided by sale amount
- `YoY Growth` — year-over-year percentage change in total sales
- `Monthly Sale Amount Trend` — monthly aggregation used as MoM workaround
- `Top Towns by Sale Amount` — towns ranked by total sale amount

---

## Known Limitations

- The dashboard uses a static CSV file and does not support live data updates
- Month-over-Month DAX growth could not be fully implemented due to multiple sales sharing the same date in the raw dataset — a Monthly Sale Amount Trend chart is used as a workaround
- The Location (GPS coordinates) field contains many null values in the raw dataset; this is expected and handled gracefully by Power Query
- Power BI Desktop is Windows-only and is required to open the `.pbix` file
