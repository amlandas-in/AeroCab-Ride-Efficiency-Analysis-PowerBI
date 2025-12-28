# 🚕 AeroCab Ride Efficiency Analysis (Power BI)

A Power BI analytics project analyzing AeroCab’s airport cab booking efficiency, ride confirmations, and delay patterns across pickup zones, segmented by peak vs non-peak hours, using Z-score based outlier analysis.

---

## 📌 Project Overview

AeroCab operates airport cab services across five major pickup zones in Bangalore. Service performance varies significantly during peak and non-peak hours, leading to booking delays, cancellations, and unconfirmed rides.

This project aims to:

- Understand ride booking behavior and confirmation trends

- Measure operational efficiency using time-based metrics

- Identify congestion-driven delays during peak hours

- Detect abnormal ride delays using statistical outlier detection

- The focus is on transforming raw operational data into clear, actionable business insights.

---

## 🔄 Data Pipeline (ETL in Power BI)

1. Extract

- Loaded raw ride-level booking data into Power BI

2. Transform

- Created key operational metrics:

  - ABT – Average Booking Time

  - ACT – Average Cab Time

  - ABOT – Average Booking Outcome Time

- Applied Z-score calculation on booking outcome time

- Binned Z-scores into 0.20 intervals

- Classified rides as:

  - Normal → Z ≤ 2

  - Outlier → Z > 2

3. Load

- Built data relationships and optimized the model for interactive dashboards

---

## 📊 Metrics Tracked

| Metric                | Description                             |
| --------------------- | --------------------------------------- |
| Total Rides           | Total number of ride requests           |
| Confirmed Rides (%)   | Successful bookings                     |
| Unconfirmed Rides (%) | Failed or dropped bookings              |
| ABT                   | Average Booking Time                    |
| ACT                   | Average Cab Arrival Time                |
| ABOT                  | Average Booking Outcome Time            |
| Z-Score Bins          | Statistical grouping for delay analysis |

---

## 🔍 Key Insights

- Peak-hour congestion is the primary driver of ride delays, with Taxi Stand and Pickup Zones consistently showing the highest impact.

- A persistent gap between ABT and ACT across all zones highlights systemic operational inefficiencies rather than isolated issues.

- Outlier rides, though few in number, disproportionately inflate average delay metrics, masking true operational performance.

- Excluding outliers reveals stable and predictable baseline operations across most pickup zones.

- Elevated unconfirmed ride rates during peak hours indicate a clear supply-demand mismatch and fleet allocation challenges.

---

## 📊 Dashboard & Analysis

- KPI cards for overall ride performance  
- ABT vs ACT comparison by pickup zone  
- Peak vs Non-Peak time segmentation  
- Z-score distribution to identify delay intensity  
- Toggle between Normal vs Outlier rides  
- Side-by-side comparison before and after removing outliers  

![image alt](https://github.com/amlandas-in/AeroCab-Ride-Efficiency-Analysis-PowerBI/blob/4df7b16082b394169a961494f2406ea8ec2fce24/assets/AeroCab_OverallDB.png)
![image alt](https://github.com/amlandas-in/AeroCab-Ride-Efficiency-Analysis-PowerBI/blob/4df7b16082b394169a961494f2406ea8ec2fce24/assets/AeroCab_OutlierDB.png)
![image alt](https://github.com/amlandas-in/AeroCab-Ride-Efficiency-Analysis-PowerBI/blob/4df7b16082b394169a961494f2406ea8ec2fce24/assets/AeroCab_ComparisonDB.png)

---

🧰 Tools & Techniques

- Power BI Desktop

- DAX (Data Analysis Expressions)

- Z-Score for Statistical Outlier Detection

- ETL Process Modeling

- KPI Cards, Bar Charts, Filters, and Slicers

---

## 📈 Business Value

- Reduces peak-hour delays by identifying congestion-heavy pickup zones and time windows

- Improves booking confirmation rates through zone-wise and time-based performance insights

- Separates true operational issues from anomalies using Z-score based outlier detection

- Supports smarter fleet allocation during peak vs non-peak demand periods

- Improves customer experience by minimizing wait times and unexpected cancellations

- Enables data-driven operational decisions instead of relying on overall averages
