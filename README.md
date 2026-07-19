# Global-Bike-Sharing-Station-Performance-Analysis
# 🚲 Global Bike Sharing Station Performance Analysis | Power BI Dashboard

## 📌 Project Overview

The **Global Bike Sharing Station Performance Analysis** project provides a comprehensive analysis of public bike-sharing station operations across multiple countries. The dashboard was developed using **Power BI** to monitor infrastructure capacity, bike availability, operational status, banking facilities, bonus stations, and geographical distribution.

The objective of this project is to transform operational bike-sharing data into meaningful business insights that help transportation authorities and bike-sharing operators optimize fleet utilization, improve customer experience, and support data-driven decision-making.

---

## 🎯 Business Problem

Bike-sharing systems generate real-time operational data from thousands of stations spread across different cities and countries. Monitoring bike availability, station capacity, operational status, and infrastructure utilization is critical for ensuring service reliability and efficient fleet management.

This project answers key business questions such as:

- How many bike-sharing stations are operational?
- Which contracts manage the largest bike-sharing networks?
- Which countries have the highest bike station capacity?
- How many bikes are currently available?
- How many docking stands are available?
- Are there inconsistencies in operational data?
- How has the network evolved over time?
- Which locations require better bike redistribution?

---

# 📊 Dashboard Overview

The Power BI dashboard provides an interactive view of the bike-sharing network using KPI cards, charts, filters, and business metrics.

### Dashboard Highlights

- 🚲 Total Bike Stand Capacity
- 🚴 Available Bikes
- 🅿 Available Bike Stands
- ⚠ Missing Bike Capacity
- 📍 Total Contracts
- 🌍 Geographic Coverage
- 🏦 Banking vs Non-Banking Stations
- 🎁 Bonus vs Non-Bonus Stations
- 📅 Year-wise Operational Trends
- 🏆 Top Performing Contracts
- 🌎 Top Performing Countries

---

# 📈 Key Performance Indicators (KPIs)

| KPI | Value |
|------|-------:|
| Total Bike Stand Capacity | **57,203** |
| Available Bikes | **19,646** |
| Available Bike Stands | **32,118** |
| Missing Bike Capacity | **5,439** |
| Total Contracts | **25** |
| State / Regions Covered | **22** |

---

# 🛠 Tools & Technologies

- **Power BI Desktop**
- **Power Query**
- **DAX (Data Analysis Expressions)**
- **Microsoft Excel**
- Data Cleaning & Transformation
- Data Modeling
- Interactive Dashboard Design

---

# 📂 Dataset Information

The dataset contains operational information for bike-sharing stations across multiple countries.

### Important Attributes

- Station Number
- Station Name
- Contract Name
- Country
- State / Region
- City
- Bike Stands
- Available Bikes
- Available Bike Stands
- Banking Facility
- Bonus Status
- Operational Status
- Last Updated Date
- Latitude & Longitude

---

# 🧹 Data Preparation

The dataset was cleaned and transformed before analysis.

### Data Cleaning

- Removed duplicate records
- Standardized column names
- Converted data types
- Extracted Year from Last Update
- Validated bike capacity calculations
- Created additional analytical columns
- Verified Boolean fields
- Checked for missing values

---

# 📐 Data Modeling

The dashboard follows a simple analytical data model.

### Fact Table

- Bike Sharing Stations

### Dimensions

- Country
- State / Region
- Contract
- Year

---

# 🧮 DAX Measures Used

```DAX
Active Bike Station =
CALCULATE(
    SUM(Sheet1[Bike Stands]),
    Sheet1[status] = "OPEN"
)
```

```DAX
Bonus Status True =
CALCULATE(
    COUNTROWS(Sheet1),
    Sheet1[bonus] = TRUE()
)
```

```DAX
Bonus Status False =
CALCULATE(
    COUNTROWS(Sheet1),
    Sheet1[bonus] = FALSE()
)
```

```DAX
Total Contracts =
DISTINCTCOUNT(Sheet1[Contract Name])
```

```DAX
Total Bike Stands (Non Banking) =
CALCULATE(
    SUM(Sheet1[Bike Stands]),
    Sheet1[banking] = FALSE()
)
```

```DAX
Total Updates 2025 =
CALCULATE(
    COUNT(Sheet1[Year]),
    Sheet1[Year] = 2025
)
```

---

# 📊 Business Insights

## 🚲 Infrastructure

- The network contains **57,203 bike stands** distributed across **25 contracts** and **22 State/Regions**.
- The widespread geographic coverage indicates strong adoption of bike-sharing services across multiple regions.

---

## 🚴 Bike Availability

- **19,646 bikes** are currently available for rental.
- **32,118 docking stands** are available for bike returns.
- The availability metrics help evaluate operational efficiency and fleet utilization.

---

## 🌍 Geographic Coverage

- The bike-sharing system operates across **22 State/Regions**, improving accessibility and supporting sustainable urban mobility.
- Expanding geographic coverage enables more commuters to access environmentally friendly transportation options.

---

## 📈 Contract Performance

Top-performing contracts based on active bike station capacity include:

| Rank | Contract | Active Bike Stands |
|------:|-----------|-------------------:|
| 1 | Lyon | 9.2K |
| 2 | Bruxelles-Capitale | 8.4K |
| 3 | Toulouse | 7.7K |
| 4 | Valence | 6.5K |
| 5 | Seville | 5.3K |

These contracts demonstrate extensive infrastructure deployment and strong operational capacity.

---

## 🌎 Country Performance

| Rank | Country | Active Bike Stands |
|------:|----------|-------------------:|
| 1 | France | 24K |
| 2 | Spain | 11K |
| 3 | Belgium | 9K |
| 4 | Ireland | 4K |
| 5 | Luxembourg | 3K |

France represents the largest bike-sharing network, reflecting strong investment in sustainable transportation infrastructure.

---

## ⚠ Data Quality Analysis

The analysis identified **5,439 missing bike stands**, representing approximately **9.5%** of the total network capacity.

### Possible Reasons

- Real-time synchronization delays
- Bike redistribution activities
- Maintenance operations
- Docking station repairs
- Temporary station outages

### Recommendations

- Implement automated validation rules.
- Increase API refresh frequency.
- Improve fleet redistribution.
- Introduce predictive maintenance.
- Monitor recurring operational inconsistencies.

---

# 📊 Analytical Approach

### Descriptive Analytics

Summarized the overall bike-sharing network, infrastructure capacity, availability, contracts, and geographic coverage.

### Diagnostic Analytics

Identified operational bottlenecks, missing bike capacity, and infrastructure utilization patterns.

### Predictive Analytics

Highlighted opportunities for demand forecasting, bike redistribution, and future network expansion.

### Prescriptive Analytics

Recommended improvements for operational efficiency, maintenance scheduling, and data quality management.

---

# 💼 Business Value

This dashboard enables stakeholders to:

- Monitor bike-sharing operations in real time.
- Optimize bike redistribution.
- Improve infrastructure utilization.
- Identify operational issues.
- Support strategic expansion decisions.
- Enhance customer satisfaction.
- Promote sustainable urban transportation.

---

# 📷 Dashboard Previ

Examples:

- Executive Dashboard
- Contract Analysis
- Geographic Analysis
- Banking & Bonus Analysis

---



---

# 👩‍💻 Author

**Dhivya Mohan**

**Data Analyst | Power BI | SQL | Excel | Python**

- Passionate about transforming data into actionable business insights.
- Experienced in Business Intelligence, Dashboard Development, Data Analysis, and Process Optimization.

---

# ⭐ If you found this project helpful

Please consider giving this repository a ⭐ to support my work.
