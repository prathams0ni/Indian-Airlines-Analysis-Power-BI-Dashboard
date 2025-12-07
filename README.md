# ✈️ Indian Airlines Analysis – Power BI Dashboard

A comprehensive and interactive **Power BI Dashboard** designed to analyze India’s domestic aviation ecosystem.  
This report transforms **120K+ rows of flight booking data** into valuable insights covering pricing trends, airline performance, customer booking patterns, route connectivity, and operational behaviors.  

This project is ideal for:
- Business Intelligence Portfolios  
- Data Analyst Job Applicants  
- Organizations analyzing airline operations  
- Students learning Power BI, DAX, and data storytelling  

---

## 📘 Project Overview

The **Indian Airlines Analysis Dashboard** helps stakeholders understand India’s domestic airline industry using analytics.  
It answers key questions such as:

- How do ticket prices behave as the travel date approaches?  
- Which airlines dominate the Indian market?  
- What are the busiest source–destination routes?  
- What times of day do passengers prefer to travel?  
- How does booking demand vary with “days left”?  

By combining meaningful KPIs, drill-down visuals, and an intuitive layout, this project demonstrates strong BI skills and analytical thinking.

---

## 🎯 Project Objectives

- Identify patterns in customer booking behavior  
- Study airline performance via booking volume and routes  
- Analyze flight pricing strategy based on demand and time-to-flight  
- Compare class and stop-wise booking distribution  
- Build a visually clean and interactive analytics dashboard  
- Demonstrate real-world Power BI capabilities for analytics roles  

---

## ✨ Key Features

- 🔹 KPI summary with key metrics  
- 🔹 Class-wise and Stop-wise Flight Distribution  
- 🔹 Dynamic pricing trend analysis (days_left vs price)  
- 🔹 Airline booking volume comparison  
- 🔹 Route matrix for intercity connectivity  
- 🔹 Time-of-day booking preference visualization  
- 🔹 Tooltip-based data exploration  
- 🔹 Optimized layout for storytelling  
- 🔹 Color-coded charts for better readability  

---

## 📊 Dashboard Walkthrough

<img width="1471" height="731" alt="image" src="https://github.com/user-attachments/assets/3313af0f-0973-4404-b19c-1df283d14e49" />

### 🟦 **Page 1 — High-Level Overview & Price Trends**

#### 🔹 KPI Metrics
- **Avg Price:** ₹7425  
- **Airlines:** 6  
- **Source Cities:** 6  
- **Avg Duration:** 11.25 hours  

#### 🔹 Class-wise Booking Split
- Economy: **68.85% (dominant)**  
- Business: **31.15%**

#### 🔹 Stop-wise Flight Split
- One-stop: **83.58%**
- Zero-stop: **12%**

#### 🔹 Price Trend by Days Left
- Prices drop steadily when customers book early  
- Indicates price elasticity based on demand  

---

<img width="1465" height="726" alt="image" src="https://github.com/user-attachments/assets/a509898a-8485-4d36-bff1-7b6e296afcb1" />

### 🟦 **Page 2 — Route, Timing & Airline Performance Analysis**

#### 🔹 Bookings by Days Left (Demand Behavior)
- Peak booking intervals: days_left 10–30  
- Minimum bookings: same-day travel (0 days left)

#### 🔹 Route Matrix (Source–Destination Heatmap)
Shows flight count between metro cities:
- Bangalore  
- Chennai  
- Delhi  
- Mumbai  
- Hyderabad  
- Kolkata  

Used for understanding route demand, fleet planning, and scheduling.

#### 🔹 Airline Booking Volume
- **Vistara:** 128K (Top performing airline)  
- **Air India:** 81K  
- **Indigo:** 43K  
- **GO_FIRST:** 23K  
- **AirAsia:** 16K  
- **SpiceJet:** 9K  

#### 🔹 Flight Timing Preferences
- Morning & Early Morning flights show highest demand  
- Evening also popular for business travelers  

---

## 📁 Data Dictionary

| Column Name | Description |
|-------------|-------------|
| airline | Airline name |
| flight | Flight number |
| source_city | Departure city |
| departure_time | Departure time category |
| stops | Zero / One stop |
| arrival_time | Arrival time category |
| destination_city | Arrival city |
| class | Business / Economy |
| duration | Flight duration in hours |
| days_left | Days between booking & flight date |
| price | Base ticket price |
| Price_gst | Final price including GST |
| days_left hist | Histogram bucket for visual |
| F1 | Row ID |

---

## 🧠 Analytical Approach

1. **Data Cleaning**  
   - Removed null values  
   - Ensured consistent format for categorical fields  
   - Verified numerical ranges (duration, prices)

2. **Feature Engineering**  
   - Created `days_left hist` for smoother visuals  
   - Derived time-of-day categories  

3. **Data Modeling**  
   - Structured into star-schema style table  
   - Optimized fields for Power BI visuals  

4. **Visual Analytics**  
   - Built KPI cards for summary  
   - Used donut charts for distribution  
   - Used line chart for pricing trend  
   - Used matrix for route connectivity  
   - Used bar charts for airline comparison  

---

## 🔍 Key Insights

- Economy class captures **~70%** of domestic bookings  
- One-stop flights dominate (*limited direct connectivity*)  
- **Ticket prices decrease** when booked earlier  
- **Vistara** has the highest booking volume  
- Metro routes show highest intercity movement  
- Morning flights are preferred by majority of passengers  
- Same-day bookings are **least common**  

---

## 🧩 Data Modeling

A simple, optimized model:

This design ensures:
- Faster load time  
- Better DAX performance  
- Clean visuals without redundancy  

---

## 📈 DAX Measures Used

DAX:
Avg Price = AVERAGE('Indian Airlines'[price])

Airlines Count = DISTINCTCOUNT('Indian Airlines'[airline])

Avg Duration = AVERAGE('Indian Airlines'[duration])

Total Bookings = COUNTROWS('Indian Airlines')

Economy % = 
DIVIDE(
    CALCULATE(COUNTROWS('Indian Airlines'), 'Indian Airlines'[class] = "Economy"),
    [Total Bookings]
)

Business % = 
DIVIDE(
    CALCULATE(COUNTROWS('Indian Airlines'), 'Indian Airlines'[class] = "Business"),
    [Total Bookings]
)

---

## ▶️ How to Run This Project

### Requirements
- Microsoft Power BI Desktop  
  Download: https://powerbi.microsoft.com/desktop/

### Steps
1. Clone this repository:
   bash:
   "git clone https://github.com/prathams0ni/indian-airlines-analysis.git"

