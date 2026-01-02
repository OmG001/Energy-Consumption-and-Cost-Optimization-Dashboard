# ⚡ Energy Consumption & Cost Optimization Dashboard

An interactive **Power BI dashboard** that analyzes **global energy consumption data** to uncover usage patterns, efficiency gaps, and cost optimization opportunities across countries and years.
This project demonstrates a complete **end-to-end business intelligence workflow**, from raw data cleaning to executive-level insights and recommendations focused on **efficiency and sustainability**.

---

## 📌 Project Overview

The project transforms raw global energy data into a visually rich and interactive dashboard that helps:

* Identify high-cost and inefficient regions
* Compare renewable vs fossil fuel energy usage
* Measure energy efficiency using per-capita metrics
* Estimate energy costs and potential savings
* Support data-driven and sustainable decision-making

---

## 🎯 Purpose of the Project

The main goals of this project are to:

* Analyze **energy consumption trends over time**
* Compare **renewable vs fossil fuel** energy usage
* Measure **energy efficiency** using per-capita metrics
* Estimate **energy costs** and identify savings opportunities
* Build an **executive-friendly Power BI dashboard**

### 📌 Suitable For

* Data analytics & BI portfolios
* Business intelligence learning
* Sustainability & energy analytics case studies

---

## 📊 Dataset Information

* **Source:** Kaggle (Open-source dataset)
* **Dataset Name:** World Energy Consumption
* **Granularity:** Country-level, yearly data

### Key Fields Used

* Country
* Year
* Total Energy Consumption
* Renewable Energy Consumption
* Fossil Fuel Consumption
* Electricity Consumption
* Population
* GDP

📌 The dataset provides both **energy and economic context**, enabling efficiency and cost analysis.

---

## 🛠 Tools & Technologies Used

### 🔹 Power BI Desktop

* Primary tool for dashboard development
* Used to build interactive visuals and reports
* Enables business-friendly insight delivery

### 🔹 Power Query

Used for data cleaning and transformation:

* Removing unnecessary columns
* Handling missing values
* Standardizing data types
* Reshaping data for analysis

**Why Power Query**

* Automates data preparation
* Ensures clean, reliable datasets
* Reduces manual preprocessing

### 🔹 DAX (Data Analysis Expressions)

Used to create dynamic measures such as:

* Total energy consumption
* Renewable energy percentage
* Energy consumption per capita
* Estimated energy cost

**Why DAX**

* Dynamic, filter-aware calculations
* Better performance
* Power BI best practices

---

## 🔄 Data Cleaning & Transformation

Performed in **Power Query Editor**:

* Removed irrelevant columns
* Handled missing and null values
* Converted year and numeric fields to correct data types
* Created derived metrics:

  * Energy per capita
  * Estimated energy cost
  * Potential savings
* Unpivoted energy columns to create:

  * `Energy Type`
  * `Energy Consumption`

📌 This transformation enables **flexible, scalable, and efficient analysis**.

---

## 🧠 Data Modelling

* Single **fact-table design** optimized for reporting
* Long-format energy data enables:

  * Easy filtering by energy type
  * Better aggregation and comparisons
* Calculations implemented as **DAX measures**, not calculated columns

**Benefits**

* Cleaner model
* Better performance
* Easier maintenance

---

## 📐 Key Metrics & Calculations

The following DAX measures convert raw data into meaningful business indicators:

* **Total Energy Consumption**
* **Total Renewable Energy**
* **Renewable Energy Percentage**
* **Energy Consumption per Capita**
* **Estimated Energy Cost**
* **Potential Cost Savings**

---

## 📊 Dashboard Pages Explained

### 📄 Page 1: Executive Overview

**Purpose:** High-level summary for decision-makers.

Includes:

* KPI cards (Total Energy, Renewable %, Estimated Cost, Potential Savings)
* Area chart for energy trends over time
* Line & stacked column chart for cost vs savings
* Country and year slicers

---

### 📄 Page 2: Energy Mix & Efficiency Analysis

**Purpose:** Identify efficiency gaps and compare countries.

Includes:

* Clustered column chart for energy mix trends
* Stacked bar chart for energy per capita by country
* Tables with conditional formatting:

  * 🔴 High energy usage
  * 🟢 High renewable adoption

---

### 📄 Page 3: Cost Optimization & Savings Opportunities

**Purpose:** Highlight actionable cost-reduction insights.

Includes:

* Energy cost KPIs
* Country-wise energy cost comparison
* Top 10 countries by renewable energy %
* Text-based analytical insights

---

## 📌 Key Insights

* Global energy consumption is steadily increasing
* Per-capita analysis reveals inefficiencies hidden in totals
* Higher renewable adoption correlates with better cost stability
* A small number of regions drive a disproportionate share of costs
* Efficiency improvements can unlock significant savings

---

## 💼 Business Value

* Supports data-driven energy planning
* Identifies inefficient and high-cost regions
* Encourages sustainable energy adoption
* Demonstrates analytics-driven cost optimization
* Useful for policy, planning, and executive decision-making

---

## ▶️ How to Use This Project

1. Download the dataset from Kaggle
2. Open **Power BI Desktop**
3. Load the dataset
4. Apply **Power Query** transformations
5. Create **DAX measures**
6. Build dashboard visuals
7. Use slicers to explore insights interactively

---

## 🧮 DAX Measures Calculations

```DAX
Total Energy =
SUM(Energy[energy_consumption])
```

```DAX
Renewable % =
DIVIDE(
    [Total Renewable Energy],
    [Total Energy]
)
```

```DAX
Energy per Capita =
DIVIDE(
    SUM(Energy[energy_consumption]),
    SUM(Energy[population])
)
```

```DAX
Estimated Energy Cost =
[Total Energy] * 0.10
```

```DAX
Potential Savings =
IF(
    [Renewable %] < 0.30,
    [Estimated Energy Cost] * 0.15,
    0
)
```

---

## 🔄 Power Query Transformations

### Unpivot Transformation

* Converted wide energy columns into long format
* Created:

  * `Energy Type`
  * `Energy Consumption`

📌 This is the **core modeling step** enabling flexible analysis.

---

## 🚀 Future Enhancements

* Add energy demand forecasting
* Integrate carbon emissions analysis
* Include real-time energy pricing
* Add drill-through and tooltip pages

---

## 📝 Project Summary

Built an interactive Power BI dashboard to analyze global energy consumption, evaluate efficiency using per-capita metrics, and identify cost optimization opportunities through renewable energy insights.

---
