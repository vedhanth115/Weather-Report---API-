# 🌦️ Weather Insights Dashboard – Power BI + API Integration

## 📌 Project Overview

This Power BI project integrates real-time weather data from a public API to deliver dynamic, city-wise weather insights across 16 major Indian cities. The dashboard features live KPIs, forecast trends, and interactive visuals that update automatically based on time and location.

Cities included:
Ahmedabad, Bangalore, Mumbai, New Delhi, Gurgaon, Hyderabad, Noida, Kolkata, Chennai, Pune, Jaipur, Kochi, Visakhapatnam, Guwahati, Mysore, Indore.

---

## 🔧 Tech Stack

- **Power BI Desktop & Service**
- **Weather API (e.g., WeatherAPI.com)**
- **Power Query (M language)**
- **DAX for dynamic measures**
- **Scheduled refresh via Power BI Service**
- **Figma**

---
### 🎨 Figma for Dashboard Design

Before building the Power BI dashboard, a visual Design was created using **Figma** to plan layout, color schemes, iconography, and user experience. This helped ensure a clean, modern design aligned with desktop responsiveness.
Figma allowed rapid iteration & implementation in Power BI, ensuring the final dashboard was both functional and visually polished.


## 🛠️ Step-by-Step Implementation

### 1. 📡 API Integration

- Used Power BI’s **Web connector** to fetch JSON data from the weather API.
- Constructed dynamic API URLs using query parameters for each city.
- Parsed nested JSON to extract:
  - `location.name`
  - `temperature`, `humidity`, `wind_speed`, `weather_description`
  - `timestamp` for time-based filtering

### 2. 🧹 Data Cleaning & Transformation

- Flattened JSON structure using **Power Query**.
- Renamed columns for clarity and consistency.
- Created a **City Master Table** for slicer control and RLS mapping.
- Removed nulls and handled API errors using conditional logic.

### 3. 📊 Data Modeling

- Created relationships between:
  - City Master ↔ Weather Data
- Defined calculated columns for:
  - `Day Timings` (Sunrise , Sunset)
  - `Weather Category` (Sunny, Rainy, Cloudy, etc.)
- Built DAX measures for:
  - `Avg Temperature`, `Max Wind Speed`, `Humidity %`, `Visibility`

### 4. 🎨 Dashboard Design

- **Live KPI Cards**: Auto-refreshing metrics for each city
- **Forecast Trends**: Line charts showing temperature and humidity over 7 Day Period
- **City Comparison**: Matrix visual comparing weather metrics across cities
- **Rain Forecast**: Bar Chart showing weather conditions
- **Slicers**: City,  Day in Week

Design principles:
- Clean, modern layout
- Color-coded weather conditions
- Responsive visuals for mobile and desktop

---

## ☁️ Cloud Deployment & Refresh

### Power BI Service Setup

- Published `.pbix` to Power BI workspace
- Configured **Scheduled Refresh**:
  - Frequency: Every hour
  - Gateway: Not required (API is cloud-accessible)
  - Credentials: API key stored securely

### Data Source Settings

- Enabled **Web API authentication**
- Used **parameterized queries** to avoid hardcoding city names
- Applied **error handling** for failed API calls
---
### 🌫️ AQI (Air Quality Index) Integration
This dashboard includes real-time AQI data for all 16 cities using a compatible environmental API. Key metrics include AQI index (0–300), main pollutant (e.g., PM2.5, NO₂), and concentration levels. Visuals are color-coded based on health impact categories, with tooltips explaining each level. AQI data is merged with weather metrics. Refresh is scheduled every hour to ensure live accuracy.


---

## 📤 Sharing & Collaboration

- Shared dashboard via **Power BI App**
- Enabled **export to PDF/PPT** for offline sharing

---

## 🚀 Highlights

- ✅ Real-time weather KPIs for 16 cities
- ✅ Fully automated refresh via cloud
- ✅ Secure access with RLS
- ✅ Mobile-optimized visuals
- ✅ API-driven architecture with scalable design

---

## 📈 Future Enhancements

- Add **historical weather trends**
- Integrate **AQI (Air Quality Index)**
- Enable **alerts for extreme weather**
- Expand to **global cities** via dynamic API parameters

---

## 👨‍💻 Author

**Vedhanth N**  
Data Analyst
🔗 [LinkedIn](https://www.linkedin.com/in/vedhanth115/)

---



