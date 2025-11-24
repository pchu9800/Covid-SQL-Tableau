# COVID-19 Data Exploration & Global Impact Dashboard (SQL + Tableau)

End-to-end COVID-19 analysis using SQL Server for data cleaning, transformation, and exploration, followed by an interactive Tableau dashboard visualizing global trends.

**Live Demo:** *https://public.tableau.com/app/profile/paulo.chu/viz/CovidDashboard_17639663301970/Dashboard1?publish=yes*

---

## 🎯 Highlights

* **Tech Stack:** SQL Server (T-SQL), Tableau
* **Workflow:** Clean → Transform → Analyze → Visualize
* **SQL Analysis Included:**
  * Total Cases vs Total Deaths (Death %)
  * Infection Rate vs Population
  * Countries with Highest Infection Rates
  * Countries with Highest Death Counts
  * Global Daily Cases/Deaths Aggregation
  * Vaccination Rolling Totals using Window Functions
  * Use of **CTEs**, **Temp Tables**, and **Views** for Tableau
* **Dashboard Visuals:**
  * Global KPIs: Total Cases, Total Deaths, Global Death %
  * Total Deaths per Continent (Bar Chart)
  * % Population Infected (2020–2021) + Forecasting
  * World Map (color-coded gradient) showing infection % by country

---

## 📁 Repository Structure

    sql-data-cleaning
    │
    ├── sql-covid.sql
    ├── covid-dashboard.twbx       
    └── README.md           


    
---

## 🚀 Quickstart

1. Clone this repo  
2. Open **covid_data_exploration.sql** in SSMS  
3. Run the scripts (includes joins, CTE, temp table, final view)  
4. Open **covid_dashboard.twbx** in Tableau Public  
5. Update data source paths if needed  
6. Publish to Tableau Public and add your link to the README  

---

## 🔧 Features in Detail

### SQL Exploration Highlights

* Analyzed COVID-19 cases, deaths, and infection rates
* Identified top countries by infection %
* Calculated global daily totals  
* Combined vaccination + death data via JOIN  
* Created running vaccination totals using:
  * `SUM() OVER (PARTITION BY ...)`
* Built reusable components:
  * `CTE (PopvsVac)`
  * `#TempTable`
  * `View: PercentPopulationVaccinated`

### Tableau Dashboard Highlights

* **KPIs:** Global cases, deaths, death percentage  
* **Charts:**
  * Deaths per Continent (Bar)
  * Forecasted Infection Rates (2020–2021)
  * Global Infection Map (blue → red gradient)
* **Interactivity:**
  * Country filters
  * Dynamic forecasting  
  * Hover tooltips for infection metrics

---

## 🗂 Data Sources

* COVIDDeaths.csv  
* COVIDVaccinations.csv  
(Pre-processed and cleaned in SQL Server)

---

## 🔮 Future Improvements

* Add 2022–2023 data  
* Connect Tableau directly to SQL Server  
* Add vaccination visualization to dashboard  

---

## 💼 Business Value

* Understand global COVID spread patterns  
* Compare continent-level death impact  
* Visualize infection concentration through geospatial mapping  
* Provide clear forecasting to anticipate trends
