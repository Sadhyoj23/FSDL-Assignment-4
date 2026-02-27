# Sales Analytics Dashboard (Beginner Guide)

This project is a simple **interactive data visualization dashboard** built using:
- **HTML** (structure)
- **CSS** (design)
- **JavaScript** (logic)
- **Chart.js** (charts)

It is designed for a real-life use case: **tracking sales trends, revenue, and profit** for an e-commerce business.

## 1. Project Goal

The dashboard helps you quickly see:
- How revenue and profit change over time
- Which product categories perform better
- Which sales channels contribute more
- Key business KPIs (Revenue, Profit, Orders, Conversion)

## 2. File Structure

- `Assignment 4/chart.html` -> Complete dashboard (HTML + CSS + JS in one file)

That single file contains everything needed.

## 3. How to Run

1. Open the folder in VS Code.
2. Open `Assignment 4/chart.html`.
3. Run with Live Server (recommended) or open directly in a browser.

If internet is available, Chart.js loads from CDN:
`https://cdn.jsdelivr.net/npm/chart.js`

## 4. Dashboard Features

### A) Filters
- **Region** dropdown: All, North, South, East, West
- **Quarter** dropdown: Q1, Q2, Q3, Q4

Changing filters updates all charts and KPI values.

### B) Simulate Button
- **Simulate New Week** creates random data changes
- Helps demonstrate real-time dashboard behavior

### C) KPI Cards
- Total Revenue
- Net Profit
- Orders
- Conversion Rate

Each KPI also shows a trend value (green for positive, red for negative).

### D) Charts Used
1. **Line Chart**: Revenue vs Profit by month
2. **Bar Chart**: Product category sales share
3. **Doughnut Chart**: Sales channel share

## 5. Data Model (Simple Explanation)

In JavaScript, data is stored in an object called `datasets`.

Structure:
- Quarter (`Q1`, `Q2`, `Q3`, `Q4`)
- Region (`north`, `south`, `east`, `west`)
- Metrics (`revenue`, `profit`, `categories`, `channels`, `orders`, `conversion`)

Example idea:
- `datasets.Q1.north.revenue` gives monthly revenue numbers for North region in Q1.

## 6. Important Functions

- `getQuarterData(quarter, region)`
  - Returns data based on selected filters
  - For "All Regions", it sums revenue/profit/orders and averages percentage shares

- `render()`
  - Updates all charts
  - Recalculates KPI cards
  - Updates "last updated" timestamp

- `jitter(array, min, max)`
  - Adds random changes to data for simulation

- `normalizeToHundred(array)`
  - Makes sure percentage arrays always total 100
  - Used for category/channel shares

## 7. UI Design Improvements Included

- Modern card-based layout
- Balanced spacing and readable typography
- Soft gradient background
- Responsive design for desktop and mobile
- Better chart section titles and helper text
- "Last updated" indicator

## 8. Beginner Learning Map

If you are new, learn in this order:
1. HTML section (page structure)
2. CSS section (how cards and layout are styled)
3. `datasets` object (where chart data comes from)
4. Chart initialization (`new Chart(...)`)
5. `render()` function (main update flow)

## 9. How to Customize

You can easily modify:
- Colors in `:root` CSS variables
- Labels in `monthLabels`, `categoryLabels`, `channelLabels`
- Data values inside `datasets`
- Chart types in `new Chart(...)`

## 10. Possible Future Enhancements

- Connect to real API data
- Add date range picker
- Add dark mode toggle
- Export charts to image/PDF
- Add table view below charts

## 11. Troubleshooting

If charts do not appear:
- Check internet connection (Chart.js CDN needed)
- Open browser console for errors
- Ensure IDs in HTML and JS match (`trendChart`, `categoryChart`, `channelChart`)

---

Created as a beginner-friendly interactive dashboard assignment project.
