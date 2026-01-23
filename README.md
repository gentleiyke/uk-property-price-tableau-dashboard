# Dynamics of England & Wales Property Market (2021–2023)

![Dashboard preview](assets/UK_Property_Price_Dashboard.png)

Interactive Tableau dashboard analysing England & Wales property sales (2021–2023) using HM Land Registry data, with KPIs and short-horizon forecasts to support market understanding and locality-level comparison.

## Live Dashboard
- Tableau Public: [add link here]
- Or open locally: `dashboard/UK_Property_Price.twbx` in Tableau Desktop or Tableau Public

## Key Insights (2021–2023)
- Leasehold sales were **<25%** of transactions, indicating a strong preference for outright ownership.  
- **Detached houses** had the highest median prices, while **terraced houses** recorded the highest sales volumes.  
- Median prices showed **£270,000** change from 2021 to 2023; sales volumes **29,370** over the same period.  
- Highest median price towns: **NORTHWOOD (£1,650,000)**, **VIRGINIA WATER (£1,647,500)**, **BURES (£1,482,500)**.  
- Forecast (8 months): median prices **rose by £39747 (£309,747)** directionally, while sales volumes showed **a spike (1,192) in June 2023** (see methodology).

> Note: Forecasts use Tableau’s built-in forecasting and are intended as directional indicators (see `docs/methodology.md`).

## What’s Included
- Tableau packaged workbook (`.twbx`) with calculated fields and dashboard
- Source dataset (`.csv`)
- Dashboard image preview

## KPIs & Metrics
- Median price (robust to outliers)
- Total properties sold (market activity)
- Geographic coverage (counties/towns)
- Sales by property category (new vs established buildings)
- Ownership/lease type distribution (leasehold vs freehold)

## How to Run / View Locally
1. Install Tableau Desktop or Login on to Tableau Public
2. Open `dashboard/UK_Property_Price.twbx`
3. Use filters (town/year) to explore price and volume trends

## Data
- Source: HM Land Registry (see acknowledgements)
- Time window: 2021–2023
- File: `data/UK-Property-Prices.csv`
- Data dictionary: `docs/data_dictionary.md`

## Repository Structure
```
uk-property-price-tableau-dashboard/
├── assets/
│   ├── UK_Property_Price_Dashboard.png  # Dashboard Image Preview
├── dashboard/
│   ├── UK_Property_Price.twbx           # Tableau Workbook with Calculated fields and dashboards
├── data/
│   ├── UK-Property-Prices.csv           # Dataset
├── docs/
│   ├── data_dictionary.md               # Data Dictionary
│   ├── methodology.md                   # Analytical and Visualisation Approach
```

## Limitations
- Land Registry coverage/latency may affect most recent months.
- Forecasts are statistical extrapolations; not a substitute for financial advice.

## Acknowledgements
HM Land Registry — for providing the underlying property transaction data.

## Contact
Ikemefula Oriaku — [LinkedIn](https://www.linkedin.com/in/gentleiyke/)

