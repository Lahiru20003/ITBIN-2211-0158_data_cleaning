# 🧼 Hotel Booking Demand Dataset – Data Cleaning Project

Welcome to the **Data Cleaning Report** for the **Hotel Booking Demand Dataset** from Kaggle. This repository showcases the full data preparation journey—from messy data to a clean, analysis-ready dataset. This is part of an academic assignment by **K L S Chandrasena (ITBIN-2211-0158)**.

---

## 📁 Dataset Overview

- **Source:** [Kaggle – Hotel Booking Demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)
- **Original Size:** 119,390 rows × 32 columns
- **File Used:** `hotel_bookings.csv`

---

## ⚠️ Issues Identified

| Category        | Columns / Examples                     | Fix Method             |
|-----------------|----------------------------------------|------------------------|
| Missing Values  | `children`, `agent`, `company`, `country` | Imputation & Filling  |
| Duplicates      | ~100+ exact duplicates                 | Removed                |
| Outliers        | `lead_time`, `adr`, `babies`           | IQR-based treatment    |
| Inconsistencies | Rows with 0 guests                     | Removed                |
| Date Formats    | `reservation_status_date`              | Converted to `datetime` |

---

## 🔧 Cleaning Steps

- 🔹 **Missing values**:
  - `children`: filled with `0`
  - `agent`, `company`: filled with `0` (interpreted as unknown)
  - `country`: filled with `"Unknown"`
  
- 🔹 **Duplicates**:
  - Removed all 100+ fully duplicated rows
  
- 🔹 **Outliers**:
  - IQR method applied on numerical columns like `adr` and `lead_time`

- 🔹 **Logical Checks**:
  - Removed rows where `adults + children + babies == 0`

- 🔹 **Date Handling**:
  - Converted relevant columns into proper `datetime` format

---

## ✅ Final Results

- 🧮 **Cleaned Rows**: ~118,800
- 🗃️ **Output File**: `hotel_bookings_cleaned.csv`
- ✅ **No missing values**
- ✅ **No duplicates**
- ✅ **All columns type-consistent and ready for analysis**

---

## 📌 Recommendations

- Improve data validation at entry level (e.g., total guests > 0)
- Ensure consistent entry of `agent` and `company` fields
- Consider standardizing country codes or replacing with ISO Alpha-3

---

## 👨‍💻 Author Info

**K L S Chandrasena**  
BSc (Hons) in Information Technology  
Index No: `ITBIN-2211-0158`  
📅 **Date:** July 30, 2025  
🌐 **GitHub:** [ITBIN-2211-0158_data_cleaning](https://github.com/Lahiru20003/ITBIN-2211-0158_data_cleaning)

---



