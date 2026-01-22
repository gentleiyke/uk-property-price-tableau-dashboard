# Methodology – UK Property Price Analysis & Forecasting

This document outlines the analytical and visualization approach used in the
UK Property Price Tableau Dashboard.

---

## Objective
To analyse property transaction trends in England & Wales (2021–2023) and provide
interactive insights into:
- Price behaviour
- Sales volume patterns
- Property type distribution
- Short-term directional forecasts

---

## Data Preparation
1. Raw HM Land Registry transaction data was filtered to the 2021–2023 period.
2. Key fields were selected (price, date, property type, tenure, location).
3. Invalid or incomplete records (e.g., missing price) were removed.
4. Date fields were transformed to support monthly aggregation.
5. Categorical fields were standardised for consistency.

---

## Aggregation Strategy
- **Median price** was used instead of mean to reduce sensitivity to outliers.
- Sales activity was measured using **transaction counts**.
- Aggregations were performed by:
  - Time (monthly, yearly)
  - Geography (county, town)
  - Property characteristics (type, tenure, new vs established)

---

## Dashboard Design
The dashboard was designed to support exploratory analysis through:
- Interactive filters (year, town)
- KPI summary tiles
- Trend visualisations (price & volume)
- Comparative bar charts by property type and ownership

Design choices prioritised clarity, interpretability, and business relevance.

---

## Forecasting Approach
- Tableau’s built-in forecasting feature was applied to **monthly aggregated metrics**.
- Forecast horizon: **8 months**
- Underlying model: Tableau’s default exponential smoothing (ETS) framework.

### Interpretation Guidance
- Forecasts are **directional**, not predictive guarantees.
- Confidence intervals (where shown) indicate uncertainty.
- Forecasts are most reliable for short-term trend direction, not exact price levels.

No external machine-learning models were trained for forecasting in this project.

---

## Validation & Limitations
- Historical trends were visually inspected for seasonality and stability.
- No hold-out test set was used for quantitative forecast validation.
- Results may be affected by:
  - Reporting delays in Land Registry data
  - Macroeconomic factors not included (interest rates, inflation)
  - Regional heterogeneity

---

## Ethical & Practical Considerations
- Analysis is descriptive and exploratory in nature.
- Outputs should not be used as financial or investment advice.
- Data usage complies with publicly available government data guidelines.

---

## Future Improvements
- Incorporate inflation-adjusted prices
- Add external variables (interest rates, CPI)
- Apply custom time-series models outside Tableau
- Extend analysis to rental markets
