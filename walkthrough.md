# Research Walkthrough

We have successfully researched, aggregated data, scored, and ranked the 10 target metropolitan statistical areas (MSAs) for rental property investment opportunity.

## Key Accomplishments

### 1. Data Aggregation & Verification
We queried and verified real-world indicators for the 10 metropolitan markets:
- **Zillow Index Data:** Pulled current typical home values (ZHVI) and typical market rents (ZORI) as of mid-2026.
- **Tax Databases:** Sourced state income tax rates (from the Tax Foundation) and local effective property tax rates per county (calculated from ACS property taxes paid vs. valuations).
- **Labor Statistics:** Fetched May 2026 unemployment rates from the Bureau of Labor Statistics (BLS).
- **Demographics:** Acquired 5-year population growth, renter ratios, and poverty rates from Census ACS profiles.
- **Education:** Sourced representative school district quality indicators.

### 2. Algorithmic Calculations
We wrote and executed a PowerShell math script ([calculate_scores.ps1](file:///C:/Users/mab07/.gemini/antigravity-ide/brain/55baddfd-b13a-4cd7-9a72-640df7ee724f/scratch/calculate_scores.ps1)) to compute:
- **Net Rental Yield:** Deducting $35\%$ operating expenses, local property taxes, and state income taxes.
- **Rentability Score ($S_{\text{rent}}$):** Weighted combination of Net Yield ($45\%$), Population Growth ($15\%$), Unemployment Inverse ($10\%$), Vacancy Inverse ($15\%$), and Renter Ratio ($15\%$).
- **Risk Score ($S_{\text{risk}}$):** Weighted combination of Unemployment ($30\%$), Poverty ($30\%$), School Deficiency ($20\%$), and Price Volatility ($20\%$).
- **Opportunity Index (REOI):** Combined score using a $0.5$ risk penalty factor.

### 3. Final Outputs & Publications
We compiled our findings and rankings into the final research analysis and tabular databases:
*   [us_rental_market_analysis.md](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/us_rental_market_analysis.md): A complete, publication-ready research report mapping all raw metrics, final scoring outputs, and detailed profiles of the best-performing and challenged markets.
*   [metro_raw_data.csv](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/data/metro_raw_data.csv): A CSV database containing all aggregated raw metrics for direct import/use in Microsoft Excel.
*   [metro_scoring_results.csv](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/data/metro_scoring_results.csv): A CSV database containing the final computed net yields, component scores, and ranking indicators.


---

## Final Rankings Summary

1.  **Charlotte, NC (REOI: 56.8):** Balanced yield, low tax burden, high growth, and low risk.
2.  **Miami, FL (REOI: 55.3):** High rentability driven by massive monthly rents ($3,200/mo) and no state income tax.
3.  **Dallas-Fort Worth, TX (REOI: 54.1):** High cash flow and rapid population growth, offsetting high property tax drag.
4.  **Atlanta, GA (REOI: 50.7):** Low risk, stable growth, and competitive yield.
5.  **Tampa, FL (REOI: 39.0):** Solid rental demand, but slightly higher local risk factors.
6.  **Phoenix, AZ (REOI: 33.8):** Moderate yield, high growth, but lower school quality averages.
7.  **New York, NY (REOI: 30.2):** High rents, but compressed yields due to steep asset prices and tax drag.
8.  **Austin, TX (REOI: 25.9):** Plagued by supply expansion, high vacancy, and high price volatility.
9.  **Chicago, IL (REOI: 24.4):** Solid cash flow offset by high property taxes ($2.10\%$) and stagnant growth ($+0.1\%$).
10. **Los Angeles, CA (REOI: -4.9):** Very low yield ($0.85\%$) due to high prices, high income tax, and declining population.

---

## Phase 2: Charlotte, NC ZIP Code Drill-Down Accomplishments

Building on Charlotte's position as our top macro investment opportunity, we completed a micro-market neighborhood analysis of 8 representative ZIP codes.

### 1. Localized Data Ingestion & Calculations
- **Zillow Indexing:** Sourced ZIP-level ZHVI (home values) and ZORI (asking rents) as of mid-2026.
- **Tax Mapping:** Calculated local property tax variation within Mecklenburg County, modeling unincorporated suburban zones (like 28277 at $0.85\%$) vs. city limits (rest of cohort at $0.95\%$).
- **Demographics & Education:** Extracted ZCTA-level population growth, renter ratios, vacancy rates, poverty rates, and public high school performance ratings.
- **Calculations:** Executed a local PowerShell scoring script ([calculate_charlotte.ps1](file:///C:/Users/mab07/.gemini/antigravity-ide/brain/55baddfd-b13a-4cd7-9a72-640df7ee724f/scratch/calculate_charlotte.ps1)) to calibrate scores against the Charlotte cohort.

### 2. Tabular & Analytical Deliverables
- [charlotte_zipcode_analysis.md](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/charlotte_zipcode_analysis.md): A comprehensive submarket report with raw metrics, scoring tables, and step-by-step mathematical walkthroughs.
- [charlotte_zip_raw_data.csv](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/data/charlotte_zip_raw_data.csv): Tabular raw data with source links for Excel vetting.
- [charlotte_zip_scoring_results.csv](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/data/charlotte_zip_scoring_results.csv): Score spreadsheet listing computed yields and ranks.

### 3. Charlotte Local Rankings Summary
1. **28273 (Steele Creek — REOI: 59.1):** Top opportunity. High renter density ($46.8\%$), strong population growth ($+11.5\%$), and a $3.19\%$ net cash-flow yield.
2. **28269 (University City — REOI: 55.3):** Highest net cash-flow yield (**3.34%**) in the local cohort, backed by UNCC student demand.
3. **28203 (South End — REOI: 41.8):** Walkable premium light-rail corridor; high pop growth and renter ratios, but compressed yield ($1.22\%$) due to high purchase prices.
4. **28277 (Ballantyne — REOI: 36.7):** Absolute safest play (Risk Score = 0.0) due to top-ranked public schools and low poverty. Stable $1.77\%$ net yield.
5. **28202 (Uptown — REOI: 36.5):** Urban core condo play; high renter ratio ($78.5\%$) but higher vacancy ($7.8\%$).
6. **28215 (East Charlotte — REOI: 33.2):** High net yield ($3.28\%$), but carries elevated socioeconomic risk.
7. **28216 (Northwest Charlotte — REOI: 25.7):** High net yield ($3.08\%$), but high poverty ($15.8\%$) and lower school quality ratings.
8. **28205 (NoDa/Plaza Midwood — REOI: 25.2):** High acquisition cost relative to standard rent averages leads to compressed yields ($1.95\%$) and lowest local ranking.

