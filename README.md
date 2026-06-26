# Cloud-Integrated AQI analysis Dashboard
An interactive Power BI dashboard analyzing **Air Quality Index (AQI) trends across multiple Indian cities**, powered by cloud-hosted data on AWS S3. Built to demonstrate scalable, decoupled analytics architecture with real-world environmental data.
 
---
 
## 📌 Project Overview
 
Air quality is one of India's most pressing environmental challenges. This project transforms raw AQI data into a visual, interactive analytics layer that lets stakeholders explore city-wise pollution patterns and track how air quality changes over time — all connected to a cloud storage backend for maintainability and scalability.
 
---
<img width="1041" height="582" alt="image" src="https://github.com/user-attachments/assets/dee02d24-efe4-40b0-a9b2-cfbc49832b75" />

 
## 🎯 Business Questions Answered
 
- Which Indian cities consistently report the highest AQI levels?
- How does AQI fluctuate across seasons and years?
- Which pollutants (PM2.5, PM10, NO2, etc.) contribute most to poor air quality in specific cities?
- How do cities compare against safe AQI thresholds defined by CPCB?
---
 
## 🏗️ Architecture
 
```
AWS S3 Bucket (Data Layer)
        │
        │  Web Data Source (URL-based connection)
        ▼
Power BI Desktop / Power BI Service
        │
        ├── Power Query  →  Data Cleaning & Transformation
        ├── DAX Measures →  KPI Calculations & Aggregations
        └── Report Layer →  Interactive Visuals & Slicers
```
 
**Key Design Decision:** The data storage and visualization layers are fully decoupled. Updating the dataset in S3 automatically reflects in the dashboard on refresh — no local file dependency, no manual re-import.
 
---
 
## Cloud Integration — AWS S3
 
| Step | Detail |
|------|--------|
| Storage | Dataset uploaded to an **AWS S3 bucket** with public read access enabled for the object URL |
| Connection | Connected to Power BI via **Web data source** using the S3 object URL |
| Transformation | Existing **Power Query** steps preserved — no transformation logic was lost during migration |
| Refresh | Dashboard can be refreshed to pull the latest version of the dataset from S3 |
 
---
 
## 📊 Dashboard Features
 
- **City-wise AQI Comparison** — Bar/column charts comparing average AQI across cities
- **Temporal Trend Analysis** — Line charts tracking AQI over months/years
- **AQI Category Breakdown** — Visual distribution across Good / Moderate / Poor / Severe categories
- **Interactive Slicers** — Filter by city, date range, and pollutant type
- **DAX Measures** — Custom calculated fields for average AQI, rolling trends, and threshold breach counts
---
 
## 🛠️ Tech Stack
 
| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard development, DAX, Power Query |
| AWS S3 | Cloud dataset storage |
| Power Query (M) | Data cleaning and transformation |
| DAX | Calculated measures and KPIs |
| Microsoft Excel / CSV | Source data format |
 
---
 

 
---
 
## 💡 Key Functionalities
 
- Provides interactive Power BI dashboards to visualize AQI trends and air quality metrics.
- Monitors major air pollutants, including PM2.5, PM10, CO, NO₂, SO₂, and O₃.
- Displays location-wise AQI information and enables comparison across different regions.
- Categorizes AQI into standard health risk levels (Good, Moderate, Poor, Very Poor, Severe).
- Tracks historical AQI trends to identify pollution patterns over time.
- Highlights key performance indicators (KPIs) for quick environmental insights.
- Integrates cloud services (if applicable) for scalable data storage and reporting.
---

