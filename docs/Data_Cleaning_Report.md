# 🧹 Data Cleaning Report  
### facebook_ad_campaign Dataset — Power BI (Power Query)

This document summarizes the full data preparation process applied to the raw Facebook ad campaign export.

---

## 📌 1. Overview of Raw Dataset  
Columns included:  
`ad_id, reporting_start, reporting_end, campaign_id, fb_campaign_id, age, gender, interest1, interest2, interest3, impressions, clicks, spent, total_conversion, approved_conversion`

Total Rows: *(depends on dataset)*

---

## 📌 2. Cleaning Steps Performed

### ✔ Step 1 — Load Raw CSV  
- Imported `facebook_ad_campaign_raw.csv` into Power Query.

### ✔ Step 2 — Remove Empty Rows  
- All rows where **all columns were null** were removed.

### ✔ Step 3 — Trim & Clean Text Columns  
Applied *Transform → Format → Trim* and *Clean* on:  
- campaign_id  
- fb_campaign_id  
- gender  
- age  
- interest fields  

### ✔ Step 4 — Convert Data Types  
- `reporting_start`, `reporting_end` → **Date**  
- `impressions`, `clicks`, `spent`, `total_conversion`, `approved_conversion` → **Whole Number / Decimal**  
- `age`, `gender`, `campaign_id`, `ad_id` → **Text**  

### ✔ Step 5 — Handle Missing Values  
- Empty `gender` and `age` values kept (useful for segmentation even if incomplete).  
- Missing numeric fields (e.g., clicks, spent) replaced with `0`.

### ✔ Step 6 — Remove Duplicates  
- Checked duplicates using `ad_id + reporting_start`.

### ✔ Step 7 — Create Cleaned Export  
Saved as `facebook_ad_campaign_cleaned.csv`.

---

## 📌 3. Final Data Quality Check  
- No null numeric metrics  
- Campaign identifiers retained  
- Consistent date formats  
- All categories cleaned and standardized  

Dataset ready for modeling in Power BI.
