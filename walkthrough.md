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
