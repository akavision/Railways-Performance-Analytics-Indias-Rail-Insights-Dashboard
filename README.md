# 🚂 Railways Performance Analytics: India's Rail Insights Dashboard

An interactive, data-driven Power BI dashboard built to analyze Indian railway performance — tracking revenue, train punctuality, passenger satisfaction, and station-level traffic across major cities.

---

## 📌 Short Description / Purpose

The Railways Performance Analytics Dashboard is a visually rich Power BI report designed to help users monitor and compare key railway metrics across train types, stations, and time periods. The dashboard covers total revenue earned, on-time vs late arrival rates, passenger satisfaction scores, and location-wise revenue distribution. It is intended for use by railway operations analysts, transport policy researchers, and data enthusiasts who want to understand Indian railway performance through data.

---

## 🛠️ Tech Stack

The dashboard was built using the following tools and technologies:

- 📊 **Power BI Desktop** – Main data visualization platform used for report creation and publishing.
- 📂 **Power Query** – Data transformation and cleaning layer including splitting columns by delimiter, removing unused columns, and reshaping raw ticket sales and performance data.
- 🧠 **DAX (Data Analysis Expressions)** – Used for 7 calculated measures: On-Time Arrival, Late Arrival, Revenue Earned, % Revenue Earned by Train Types, % Train Traffic at Railway Stations, % Revenue Earned by Location, and Satisfaction by Train Type.
- 📅 **Date_Lookup Table** – A custom Calendar Dimension built in DAX with Date, Day, Month, MonthName, Quarter, and Year columns to enable time intelligence and period filtering.
- 🗺️ **Bing Maps Integration** – Used for geo-mapping revenue distribution across Indian cities (Delhi, Chennai, Mumbai, Kolkata).
- 📁 **File Format** – `.pbix` for development; `.png` for dashboard previews.

---

## 📂 Data Source

**Source:** Simulated Indian Railways operational dataset (2022)

The data model consists of **5 tables** with relationships established across fact and dimension tables:

**TicketSalesData** (Fact Table)
- `Date`, `Date_Only` – Transaction date fields
- `Number of Tickets Sold` – Daily ticket volume
- `Station ID (Departure)` – Departure station reference

**TrainPerformanceData** (Fact Table)
- `Date` – Performance observation date
- `On Time Arrival` – Punctuality metric
- `Passenger Satisfaction` – Satisfaction score per train
- `Train ID` – Train reference key

**Train_Lookup** (Dimension)
- `Train ID`, `Train Type` – Train classification (Rajdhani, Vande Bharat, Duronto, Shatabdi, Garib Rath Express)
- `Average Per Seat Price` – Pricing data
- `Number of Coaches` – Capacity indicator

**Station_Lookup** (Dimension)
- `Station ID`, `Station Name` – Station identifiers
- `Location` – City (Delhi, Chennai, Mumbai, Kolkata)
- `Capacity` – Station handling capacity

**Date_Lookup** (Date Dimension)
- `Date`, `Day`, `Month`, `MonthName`, `Quarter`, `Year`

**Measures_Table** – A dedicated table housing all DAX measures for clean model organization.

---

## ✨ Features / Highlights

### 🔴 Business Problem

Indian Railways is one of the world's largest rail networks, yet performance data across train types and stations is rarely presented in an accessible, visual format. Key operational questions such as:

- Which train types generate the most revenue?
- How does on-time performance vary across train categories?
- Which stations handle the most traffic?
- How does passenger satisfaction differ by train type?
- How has revenue trended over time?

...are difficult to answer quickly without an interactive analytical tool.

---

### 🎯 Goal of the Dashboard

To deliver an interactive visual tool that:

- Tracks total revenue and breaks it down by train type and location.
- Compares on-time vs late arrival rates across all major train categories.
- Monitors passenger satisfaction scores by train type.
- Analyzes station-level traffic distribution across major railway hubs.
- Enables time-period filtering to study monthly and quarterly performance trends.

---

### 📊 Walkthrough of Key Visuals

**🔢 Key KPIs (Left Panel)**
- **Total Revenue Earned:** ₹1.50bn
- **Total Stations Covered:** 4
- **Different Stations Covered:** 5

**🍩 % of Revenue Earned by Train Type (Donut Chart)**
Breakdown of revenue contribution by train category:
- Rajdhani Express: 30%
- Duronto Express: 26.59%
- Vande Bharat Express: 19.72%
- Shatabdi Express: 13.75%

**🍩 % of Train Traffic at Different Railway Stations (Donut Chart)**
Station-wise traffic distribution across major hubs:
- Chhatrapati Shivaji (Mumbai): 25.2%
- New Delhi Railway Station: 25.2%
- Howrah Junction (Kolkata): 24.8%
- Chennai Central: 24.8%

**📊 On-Time vs Late Arrival by Train Type (Column Chart)**
Side-by-side comparison of punctuality across train types. Vande Bharat Express leads with 83 on-time arrivals, while Garib Rath Express shows the lowest at 47 — highlighting performance gaps across categories.

**📊 Satisfaction by Train Type (Bar Chart)**
Passenger satisfaction scores ranked by train type:
- Vande Bharat Express: Highest (~68)
- Garib Rath Express: ~62
- Rajdhani Express: ~62
- Duronto Express: ~60
- Shatabdi Express: ~55

**🗺️ % of Revenue Earned Location Wise (Map Visual)**
Geo-mapped bubble chart showing revenue concentration across Delhi, Chennai, Mumbai, and Kolkata.

**📈 Revenue Earned Over Time (Line Chart)**
Daily revenue trend line spanning January 2022 to December 2022, showing fluctuations and seasonal patterns across the full year.

**🎛️ Time Period Filter (Date Slicer)**
A date range slicer (01-01-2022 to 31-12-2022) allows users to filter all visuals by any custom time period dynamically.

---

### 💡 Business Impact & Insights

- **Revenue Optimization:** Rajdhani Express contributes the highest revenue share (30%), making it the most commercially critical train type — a key focus for capacity and pricing strategy.
- **Punctuality Gaps:** Vande Bharat Express leads in on-time arrivals while Garib Rath Express lags — indicating where operational improvements are needed most.
- **Passenger Experience:** Satisfaction scores correlate with train quality — premium trains (Vande Bharat, Rajdhani) score higher, suggesting investment in lower-tier trains could improve overall ratings.
- **Balanced Station Traffic:** All four major stations handle roughly equal traffic (~25% each), indicating efficient load distribution across the network.
- **Seasonal Revenue Trends:** The time-series line chart enables identification of revenue dips and spikes across months, supporting demand-based scheduling decisions.

---

## 📸 Dashboard Preview

![Railways Performance Analytics Dashboard](preview.png)

---

## 🚀 How to Use

1. Download and open `RailwayUltimateProject.pbix` in **Power BI Desktop**.
2. Use the **Time Period slicer** to filter data by any custom date range.
3. Click on any donut chart segment to cross-filter all related visuals.
4. Hover over map bubbles to see city-level revenue details.
5. Compare on-time vs late arrival bars to identify punctuality patterns by train type.

---

*Built by Akhilesh Madwalkar | Power BI | DAX | Data Analytics*
