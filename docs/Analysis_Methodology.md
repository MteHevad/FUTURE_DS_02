# 📈 Analysis Methodology  
### Power BI Campaign Performance Dashboard

This document outlines the approach used to analyze Facebook ad campaign performance.

---

## 1. Data Import & Data Model
- Loaded the cleaned dataset from `/data/facebook_ad_campaign_cleaned.csv`.
- Fact table: **Campaign** (single table model)
- Date columns connected using auto-date hierarchy in Power BI.

---

## 2. DAX Measures  
Created a metrics layer using calculations for:
- CTR  
- CPC  
- CPM  
- Conversion Rate  
- Spend Efficiency  
- ROI  
- Aggregated totals (Clicks, Impressions, Spend)

All DAX formulas are included in `../powerbi/DAX_Measures.txt`.

---

## 3. Analytical Dimensions
Segmented results by:
- Age groups  
- Gender  
- Three interest categories  
- Ad ID  
- Campaign ID  
- Reporting period  

---

## 4. Visual Analytical Views

### ✔ KPI Summary View  
High-level performance metrics (CTR, CPC, CPM, Conversions).

### ✔ Trend View  
Line charts showing:
- Impressions trend  
- Spend trend  
- CTR trend  

### ✔ Top Ads View  
Ranked by:
- Clicks  
- Conversions  
- Spend efficiency  

### ✔ Audience Breakdown  
Bar and donut charts for:
- Conversions by gender  
- CTR by age group  
- Interest performance  

---

## 5. Insights Development  
From the dashboard visuals, insights were extracted based on:
- High-performing demographics  
- Cost-efficient ads  
- Conversion bottlenecks  
- Interest-based variability  

These insights are documented in `Insights_Report.md`.

---

## 6. Deliverables  
- Fully interactive dashboard (`Campaign_Performance_Dashboard.pbix`)  
- Exported PDF dashboard (`Campaign_Performance_Dashboard.pdf`)  
- Final report (`Task2_Report.pdf`)
