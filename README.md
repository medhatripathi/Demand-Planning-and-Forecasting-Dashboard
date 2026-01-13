# 📋 Demand-Planning-and-Forecasting-Dashboard
An end-to-end Excel-based demand forecasting and sales analytics solution that analyzes 2 years of weekly sales data (520 records) to identify seasonality patterns, measure promotional effectiveness, quantify stockout impact, and generate 13-week forecasts for Q1 2025 with accuracy validation. 
(https://docs.google.com/spreadsheets/d/17-YqmPPd4YnestEh2aFN6yTQm_plnswtlwqnnKURbQY/edit?usp=sharing)

# 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| **Microsoft Excel** |	Primary analysis platform |
| **SUMIFS / AVERAGEIFS** |	Conditional aggregations |
| **FORECAST.LINEAR** |	Time series forecasting |
| **Pivot Tables** | Data summarization & exploration |
| **Conditional Formatting** | Visual accuracy indicators |
| **Excel Charts** |	Dashboard visualizations |

# 📁 Data Source

**Dataset Overview**

| Attribute |	Details  |
|------|---------|
| Time Period |	January 2023 – December 2024 |
| Total Records	| 520 rows |
| Granularity	| Weekly |
| SKUs Covered |	5 products |
| Categories	| Tissue, Paper Towels, Facial Tissue, Napkins |

**Built-in Data Patterns**

  - 📈 Holiday Season Lift: November-December (+35%)
  - 📉 Post-Holiday Dip: January (-15%)
  - 🎯 Promotional Lift: ~40% increase during promotions
  - ⚠️ Stockouts: ~5% of periods affected
  - 📊 Growth Trend: Gradual YoY growth over 2 years

# ✨ Features & Highlights
### 🎯 Business Problem

**Colors Tissue and Hygiene Products faces critical supply chain challenges:**

  - Demand Volatility: Significant fluctuations in weekly sales make inventory planning difficult
  - Seasonal Uncertainty: Holiday and post-holiday demand swings cause over/under-stocking
  - Promotional Impact: Lack of quantified promotional effectiveness leads to poor planning
  - Stockout Costs: Unquantified revenue losses from inventory shortages
  - Forecasting Gap: No systematic approach to predict future demand

### 🎯 Dashboard Goals
| Goal |	Deliverable |
|------|---------|
| Analyze Historical Performance | Sales breakdown by SKU, category, and time period |
| Identify Seasonality Patterns |	Monthly indices for demand planning |
| Measure Promotional Effectiveness |	Lift percentages by product |
| Quantify Stockout Impact |	Revenue loss estimation |
| Generate Accurate Forecasts |	13-week Q1 2025 predictions |
| Validate Forecast Accuracy |	MAPE calculations with visual indicators |

# 📊 Dashboard Walkthrough

### Phase 1: Data Analysis
**Key Metrics Calculated:**

  - Total Units Sold (2023 vs 2024)
  - Total Revenue by SKU
  - Average Weekly Sales
  - Sales Contribution %

**Impact Assessment:**

  - Total stockout events identified
  - Revenue loss estimation
  - Products most affected
    ![Phase1_Data Analysis](https://github.com/medhatripathi/Demand-Planning-and-Forecasting-Dashboard/blob/main/Phase1_Data%20Analysis.png)

### Phase 2: Forecast Development

| Method |	Formula |	Use Case |
|------|---------|---------|
| 4-Week Moving Average |	=AVERAGE(OFFSET($H$2, ROW()-5, 0, 4, 1)) |	Short-term smoothing |
| Seasonality-Adjusted | =Average_Sales * Seasonal_Index * (1 + Growth_Rate) |	Pattern-based forecasting |
| Linear Regression |	=TREND(Known_X, Known_Y, Future_Period)	| Trend projection |
![Phase2_Forecast Development](https://github.com/medhatripathi/Demand-Planning-and-Forecasting-Dashboard/blob/main/Phase2_Forecast%20Development.png)

### Phase 3: Accuracy & Insights

**Testing Period: Last 13 weeks of 2024 (Q4 2024)**

- Absolute Percentage Error: =ABS((Actual - Forecast) / Actual)
- MAPE: =AVERAGE(Absolute_Percentage_Error_Range)
- Forecast Accuracy: =1 - MAPE

**Conditional Formatting Rules**

| Accuracy Level	| MAPE Range |	Color Code  |
|------|---------|---------|
| High Accuracy	| < 10%	| 🟢 Green  |
| Moderate Accuracy |	10% - 20%	| 🟡 Yellow  |
| Low Accuracy	| > 20%	| 🔴 Red  |
![Phase3_Accuracy & Insights](https://github.com/medhatripathi/Demand-Planning-and-Forecasting-Dashboard/blob/main/Phase3_Accuracy%20%26%20Insights.png)

### Phase 4: Dashboard & Recommendations

**Dashboard Components**
- **Forecast Accuracy Tables:** Conditional formatted MAPE display
- **Promotional Impact Summary:** Lift percentages by product
- **Stockout Analysis:** Events and estimated losses

**Pivot Table Configurations**
**Sales by Month:**
- Rows: Month | Values: Sum of Units_Sold
**Sales by SKU and Year:**
- Rows: SKU | Columns: Year | Values: Sum of Units_Sold
**Promo vs Non-Promo Performance:**
- Rows: SKU | Columns: Promotion | Values: Average of Units_Sold
![Phase4_Dashboard & Recommendations](https://github.com/medhatripathi/Demand-Planning-and-Forecasting-Dashboard/blob/main/Phase4_Dashboard%20%26%20Recommendations.png)

# 💡 Business Impact & Insights
### Key Findings

  **Seasonal Demand Patterns**
       - Peak season (Nov-Dec) drives 35% higher demand
       - January requires inventory reduction planning (-15%)

  **Promotional Effectiveness**
      - Average promotional lift: ~40%
      - Optimal for demand smoothing during slow periods

  **Stockout Analysis**
      - ~5% of periods affected
      - Highest impact on SKU-1004 (Napkins)
      - Estimated revenue loss: $X,XXX

  **Growth Trajectory**
      - Positive YoY growth trend across all SKUs
      - Category leaders: Tissue (+X%), Paper Towels (+X%)
