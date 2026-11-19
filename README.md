# 🥤 FreshFlow Sales Dashboard

An interactive web dashboard showing 30 days of sales for **FreshFlow**, a fresh-juice and smoothie brand with several outlets.

## 🔗 Live Dashboard

**👉 [https://freshflow-dashboard.planar-maps.workers.dev/](https://freshflow-dashboard.planar-maps.workers.dev/)**

The dashboard is hosted on Cloudflare Workers. Open the link in any modern browser; you don't need to install or sign in to anything.

---

## 📌 Project Details

### Objective
Turn FreshFlow's raw sales transactions into a clear, interactive dashboard. It helps the business answer questions like these:
- How much revenue and profit did we make, and how did it change from day to day?
- Which outlets, categories and products bring in the most revenue?
- Which payment methods do customers prefer?
- How do discounts affect sales?

### Dataset

| Item | Detail |
|------|--------|
| Time period | 30 days (Week 1 – Week 5) |
| Transactions | 4,977 orders |
| Units sold | 13,599 |
| Currency | Indian Rupees (₹) |

**Each transaction includes:** day, week, outlet, category, product, payment method, discount band, quantity, gross sales, discount amount, net revenue, cost and gross profit.

### Methodology
1. **Data cleaning:** Mapped coded values (outlet, category and payment) to readable labels.
2. **Feature engineering:** Calculated net revenue (gross sales − discount) and gross profit (net revenue − cost). Grouped each order's discount into a band (No discount, 1–10%, 11–20%, 21–25% or Above 25%).
3. **KPI calculation:** Added up revenue, profit, cost, discount, orders and units for any filtered selection.
4. **Visualisation:** Built an interactive dashboard with filters, KPI cards and 7 charts.
5. **Deployment:** Published it as a single web page on Cloudflare Workers.

---

## 📊 Dashboard Details

### Filters
Choose any combination of filters. Every KPI and chart updates right away:

| Filter   | Options |
|----------|---------|
| Outlet   | Outlet A, Outlet B, Outlet C, Other |
| Category | Coconut Water, Detox, Fresh Juices, Smoothies |
| Payment  | Card, Cash, UPI, Wallet |
| Product  | Apple Juice, Berry Smoothie, Coconut Water, Green Detox, Mango Smoothie, Orange Juice, Pineapple Juice, Watermelon Juice |
| Week     | Week 1 – Week 5 |

A status line shows how many transactions match the current filters. The **Reset** button clears all filters.

### KPI Cards (overall values)

| KPI | Value |
|-----|-------|
| Net Revenue | ₹10,89,757 |
| Gross Profit | ₹5,34,526 (≈ 49% margin) |
| Orders | 4,977 |
| Units Sold | 13,599 |
| Gross Sales | ₹11,70,024 |
| Total Discount | ₹80,267 |
| Total Cost | ₹5,55,232 |

### Charts

| Chart | Type | What it shows |
|-------|------|---------------|
| Revenue Growth | Line | Net revenue for each day across the 30 days |
| Revenue by Category | Pie | Revenue share by product category |
| Order Activity | Area | Number of orders per day |
| Payment Share % | Doughnut | Revenue split by payment method |
| Revenue by Product | Bar | Net revenue for each product |
| Discount Impact | Horizontal bar | Revenue by discount band |
| Revenue by Outlet | Bar | Net revenue for each outlet |

---

## 💡 Key Insights

- **Outlet A is the top outlet.** It earned 40.2% of revenue (₹4.38 L), followed by Outlet B (34.6%) and Outlet C (25.2%).
- **Fresh Juices bring in the most revenue,** with 56.4% of the total. Smoothies are next with 30.0%.
- **Apple Juice (₹2.05 L) and Orange Juice (₹1.99 L) are the best-selling products.** Together they make up about 37% of revenue.
- **UPI is the most-used payment method,** with 50.6% of revenue. Card (20.0%) and Cash (19.4%) are well behind.
- **Discounts are used carefully.** About 49% of revenue came from orders with no discount, and almost no orders had a discount above 25%.
- **Week 2 was the strongest week** (₹2.85 L). Week 5 is low because it covers only the last 2 days.
- **Average order value is about ₹219,** and the gross profit margin is about 49%.

---

## 🛠️ Tech Stack

- **HTML / CSS / JavaScript**: a single, self-contained page
- **[Chart.js 4.4.1]:** draws the charts
- **Cloudflare Workers**: hosting
- **Responsive layout**: works on desktop, tablet and mobile

## 📝 Notes

Category, payment and outlet names are display labels mapped from coded values in the source data.
