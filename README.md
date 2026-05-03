# 🚲 Cyclistic Bike-Share Analysis
### Google Data Analytics Capstone — Case Study 1

---

## 📌 Background

Cyclistic is a fictional bike-share company in Chicago with over 5,800 bikes and 600 docking stations. The marketing director believes that converting **casual riders into annual members** is key to future growth.

As a junior data analyst, I was tasked with answering:

> **How do annual members and casual riders use Cyclistic bikes differently?**

---

## 🗂️ Data Source

- **Divvy Trips 2019 Q1** and **Divvy Trips 2020 Q1**
- Provided by Motivate International Inc. under a [public license](https://divvybikes.com/data-license-agreement)
- ~800,000 combined ride records

---

## 🔧 Tools Used

| Tool | Purpose |
|------|---------|
| Python | Data cleaning, analysis, visualisation |
| Pandas | Data wrangling & aggregation |
| Matplotlib / Seaborn | Charts and visual outputs |

---

## ⚙️ Process

### 1. Prepare
- Downloaded and inspected both quarterly datasets
- Identified schema differences between 2019 and 2020 files

### 2. Process
- Renamed 2019 columns to match 2020 schema
- Harmonised user type labels (`Subscriber → member`, `Customer → casual`)
- Engineered new features:
  - `ride_length` — duration in minutes
  - `day_of_week` — day the ride started
  - `hour` — hour of day the ride started
- Removed rows with negative or zero ride lengths

### 3. Analyze
- Descriptive statistics by user type
- Ride counts and average durations by day of week
- Ride volume by hour of day
- Distribution of ride lengths

---

## 💡 Key Findings

1. **Members ride more frequently** but for shorter durations — consistent with commuting behaviour.
2. **Casual riders ride longer** (roughly 2–3× on average) and concentrate trips on **weekends** — consistent with leisure use.
3. **Members show strong 8 AM and 5 PM spikes** in hourly usage, a clear commuter pattern absent in casual riders.

---

## ✅ Top 3 Recommendations

### 1. 📅 Weekend Membership Promotion
Target casual riders on Saturdays and Sundays with digital ads showing the cost savings of an annual membership versus single-ride passes.

### 2. 🚆 Commuter Conversion Campaign
Identify casual riders who already ride on weekdays and send them personalised offers showing exactly how much they'd save commuting with an annual membership.

### 3. 🌤️ Trial / Seasonal Membership Tier
Introduce a lower-commitment "Summer Pass" or trial membership to reduce the barrier to sign-up. Once riders experience membership benefits, full conversion becomes more likely.

---

## 📁 Repository Structure

```
cyclistic-bike-share-case-study/
├── cyclistic_analysis.py       # Full analysis script
├── README.md                   # This file
└── outputs/
    ├── 01_total_rides_by_user_type.png
    ├── 02_avg_ride_length_by_user_type.png
    ├── 03_rides_by_day_of_week.png
    ├── 04_avg_ride_length_by_day.png
    ├── 05_rides_by_hour_of_day.png
    ├── 06_ride_length_distribution.png
    └── summary_stats.csv
```

---

## 🚀 How to Run

```bash
# Install dependencies
pip install pandas matplotlib seaborn

# Place the two CSVs in the same folder, then run:
python cyclistic_analysis.py
```

---

*This project was completed as part of the [Google Data Analytics Professional Certificate](https://grow.google/certificates/data-analytics/) capstone.*
