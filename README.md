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

Extract

- Loaded raw ride-level booking data into Power BI

Transform

- Created key operational metrics:

  - ABT – Average Booking Time

  - ACT – Average Cab Time

  - ABOT – Average Booking Outcome Time

- Applied Z-score calculation on booking outcome time

- Binned Z-scores into 0.20 intervals

- Classified rides as:

  - Normal → Z ≤ 2

  - Outlier → Z > 2

Load

- Built data relationships and optimized the model for interactive dashboards
