# Data Dictionary – UK Property Prices (England & Wales)

This document describes the structure, fields, and derived variables used in the
UK Property Price Tableau Dashboard.

## Source
- HM Land Registry – Price Paid Data
- Time period covered: 2021–2023
- Geographic scope: England & Wales

---

## Core Fields (Raw Data)

| Column Name | Data Type | Description |
|------------|----------|-------------|
| transaction_id | String | Unique identifier for each property transaction |
| price | Integer | Sale price of the property in GBP (£) |
| date_of_transfer | Date | Official date the property transaction was completed |
| postcode | String | Postal code of the property |
| property_type | Categorical | Property classification: Detached, Semi-Detached, Terraced, Flat |
| new_build_flag | Boolean | Indicates whether the property is newly built |
| tenure | Categorical | Ownership type: Freehold or Leasehold |
| locality | String | Town or locality of the property |
| district | String | Administrative district |
| county | String | County where the property is located |

---

## Derived / Calculated Fields

These fields were created during data preparation or within Tableau to support analysis.

| Field Name | Description |
|-----------|-------------|
| year | Extracted from `date_of_transfer` |
| month | Extracted from `date_of_transfer` |
| year_month | Monthly aggregation key for trend and forecasting analysis |
| property_category | Derived from `new_build_flag` (“New” vs “Established”) |
| ownership_type | Normalised tenure grouping (Leasehold / Freehold) |
| median_price | Median transaction price at selected aggregation level |
| total_sales | Count of transactions at selected aggregation level |

---

## Data Quality Notes
- Prices are nominal and not inflation-adjusted.
- Duplicate transaction IDs were removed.
- Records with missing or invalid prices were excluded.
- Postcodes were used only for geographic grouping, not exact geospatial mapping.

---

## Intended Use
This dataset is designed for:
- Market trend analysis
- Regional price comparison
- Volume vs value exploration
- Short-term directional forecasting

It is **not** intended for individual property valuation or financial advice.

