# Uber Ride Analytics Dashboard 2024

End-to-end data analytics project analyzing ride-sharing operational performance, cancellation behavior, revenue distribution, and customer satisfaction using Python for data processing and Tableau Public for interactive visualization.

---

## Project Overview

This project analyzes a 2024 ride-sharing dataset containing approximately 150,000 bookings. The objective is to transform raw operational ride data into structured business insights through data cleaning, feature engineering, exploratory data analysis, and interactive dashboard development.

The final deliverable is a dynamic dashboard with three analytical sections:

1. Executive Overview  
2. Operational Performance  
3. Revenue & Customer Insights  

---

## Business Objectives

This project aims to answer the following questions:

- What is the overall operational health of the platform?
- What factors influence ride cancellations?
- Which vehicle categories generate the highest revenue?
- Does operational efficiency impact customer satisfaction?
- Where are the key performance bottlenecks?

---

## Tools & Technologies

- Python
  - pandas
  - numpy
  - matplotlib (for EDA support)
- Tableau Public
- GitHub (version control)

---

## Dataset Overview

- Total Bookings: ~150,000
- Time Period: January – December 2024
- Vehicle Types:
  - Auto
  - Bike
  - eBike
  - Go Mini
  - Go Sedan
  - Premier Sedan
  - Uber XL

### Key Variables

- Booking Status
- Avg VTAT (Driver arrival time)
- Avg CTAT (Trip duration)
- Booking Value
- Ride Distance
- Cancellation Reason (Customer & Driver)
- Driver Ratings
- Customer Ratings
- Payment Method

---

## Data Cleaning & Feature Engineering (Python)

Data preprocessing was performed using pandas.

### Key Transformations

- Converted Date and Time columns to proper datetime format
- Created unified datetime column
- Extracted:
  - Hour
  - Day of Week
  - Weekend indicator
- Created performance flags:
  - is_completed
  - is_cancelled
- Engineered business metrics:
  - Completion Rate
  - Cancellation Rate
  - Revenue per KM
  - Trip duration category

### Example Business Calculations

Cancellation Rate:
SUM(is_cancelled) / COUNT(Booking ID)

Revenue per KM:
Booking Value / Ride Distance

---

## Exploratory Data Analysis

Key findings from EDA:

- Overall cancellation rate is approximately 25%
- Completion rate is approximately 62%
- Customer cancellations are higher than driver cancellations
- VTAT variations across vehicle types correlate with cancellation levels
- Revenue contribution differs significantly between vehicle categories

---

## Dashboard Architecture (Tableau)

The final dashboard uses parameter-based dynamic section control to switch between analytical views within a single layout.

### 1. Executive Overview

- Total Bookings
- Completion Rate
- Cancellation Rate
- Total Revenue
- Monthly Booking Trend
- Cancellation Breakdown

Purpose: High-level KPI monitoring.

---

### 2. Operational Performance

- Cancellation Rate by Hour
- Cancellation Heatmap (Hour vs Day)
- Average VTAT by Vehicle
- Booking Status Distribution

Purpose: Identify operational inefficiencies and peak risk periods.

---

### 3. Revenue & Customer Insights

- Revenue by Vehicle
- Revenue per KM
- VTAT vs Cancellation (Scatter Analysis)
- Rating by Vehicle Type

Purpose: Evaluate profitability versus service quality trade-offs.

---

## Key Insights

1. Cancellation behavior is time-sensitive and clustered around specific hours.
2. Higher driver arrival time (VTAT) correlates with increased cancellation probability.
3. Revenue concentration is uneven across vehicle categories.
4. Revenue efficiency (per KM) varies significantly across segments.
5. Operational efficiency impacts customer experience metrics.

---

## Live Dashboard

Tableau Public Link:   
https://public.tableau.com/app/profile/musalim.ridho/viz/uberDashboard_17719553429340/MasterDashboard   