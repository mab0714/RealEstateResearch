# Implementation Plan - US Rental Market Direct Research & Analysis

This project shifts focus from building a software application to performing direct research and data aggregation for a selection of representative U.S. metropolitan markets. We will gather real-world data through web queries, apply our scoring models, and rank these markets for rentability and risk.

---

## Targeted Metropolitan Areas

We will aggregate data for a balanced selection of major U.S. markets representing different tax structures and economic profiles:

1. **Dallas-Fort Worth, TX** (No state income tax, high property tax, high growth)
2. **Miami-Fort Lauderdale, FL** (No state income tax, moderate property tax, high growth)
3. **Phoenix-Mesa, AZ** (Low flat state income tax, low property tax, high growth)
4. **Charlotte-Concord, NC** (Flat state income tax, moderate property tax, stable growth)
5. **Atlanta-Sandy Springs, GA** (Flat state income tax, moderate property tax, stable growth)
6. **Chicago-Naperville, IL** (Flat state income tax, very high property tax, low growth)
7. **Los Angeles-Long Beach, CA** (High graduated state income tax, low property tax, declining growth)
8. **New York-Newark, NY/NJ** (High state income tax, high property tax, mature market)
9. **Austin, TX** (No state income tax, high property tax, high price-to-rent volatility)
10. **Tampa-St. Petersburg, FL** (No state income tax, moderate property tax, high rental demand)

---

## Research Tasks & Data Collection

For each target metropolitan area, we will perform web queries to compile:

| Metric | Primary Public Data Source | Description |
| :--- | :--- | :--- |
| **Typical Home Value** | Zillow Research (ZHVI) | Median single-family home value for 2026/latest |
| **Typical Monthly Rent** | Zillow Research (ZORI) | Median market-rate asking rent for 2026/latest |
| **Effective Property Tax** | Tax Foundation / Census | State/local average effective property tax rate |
| **State Income Tax** | Tax Foundation | Top marginal state individual income tax rate |
| **Unemployment Rate** | Bureau of Labor Statistics (BLS) | Local metro unemployment rate (latest 2026) |
| **5-Yr Population Growth** | Census ACS | Population change rate from 2018/2019 to 2024/2026 |
| **Poverty Rate** | Census ACS | Local poverty percentage |
| **School Quality Index** | NCES / State reports | General school system rank/student ratio indicator |

---

## Analytical Scoring Models

Using the aggregated data, we will calculate:

1. **Net After-Tax Yield ($Y_{\text{net}}$):**
   - Assumes a standard $35\%$ operating expense ratio.
   - Deducts effective local property taxes.
   - Deducts state individual income taxes.
2. **Rentability Score ($S_{\text{rent}}$):** Weighted combination of Net Yield ($45\%$), Population Growth ($15\%$), Job/Employment Growth ($10\%$), Rental Occupancy ($15\%$), and Renter Ratio ($15\%$).
3. **Risk Score ($S_{\text{risk}}$):** Weighted combination of Local Unemployment ($30\%$), Poverty Rate ($30\%$), School Quality ($20\%$), and Price Volatility ($20\%$).
4. **Real Estate Opportunity Index (REOI):** $S_{\text{rent}} - 0.5 \cdot S_{\text{risk}}$

---

## Open Questions

- Are there any other specific metro areas or cities you would like to swap into or out of this list?
- For the qualitative landlord-friendliness factor, would you like us to add it as a risk multiplier or keep it separate as a descriptive label?

---

## Deliverables

### [Research Outputs]

#### [NEW] [us_rental_market_analysis.md](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/us_rental_market_analysis.md)
The final research paper and dataset, containing detailed market tables, calculated scores, scatter plots, and an investment recommendation ranking.
