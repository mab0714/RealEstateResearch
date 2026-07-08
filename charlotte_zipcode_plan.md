# Drill-Down Implementation Plan - Charlotte, NC ZIP Code Analysis

This research transitions our analysis from a macro metropolitan comparison to a micro-level neighborhood comparison within **Charlotte, NC** (Mecklenburg County). We will target 8 representative ZIP codes to evaluate local cash-flow yields, school quality, socioeconomic risk, and overall rental viability.

---

## Targeted ZIP Codes

We will analyze a diverse cross-section of Charlotte sub-markets:

1.  **28203 (South End / Dilworth):** Premium urban market; high-density, trendy, high asset pricing, low yields.
2.  **28202 (Uptown):** Core central business district; high-rise condos, high renter concentration.
3.  **28205 (NoDa / Plaza Midwood):** Hip, historic, high-demand single-family and multifamily rental market.
4.  **28269 (University City / North Charlotte):** Large suburban area close to UNC Charlotte; moderate home prices, strong student/young professional demand.
5.  **28277 (Ballantyne):** Highly affluent southern suburb; low risk, top-performing public schools, premium single-family rentals.
6.  **28215 (East Charlotte):** Emerging suburban area; lower home values, higher cash-flow yields, moderate risk.
7.  **28216 (Northwest Charlotte / Beatties Ford):** Developing/gentrifying area; lower buy-in cost, higher potential yield, higher economic risk.
8.  **28273 (Steele Creek / Southwest):** Suburb near airport and logistics employment centers; high renter ratio, stable demand.

---

## Data Collection & Calibration

For each ZIP code, we will collect local indicators:

| Metric | Source | Local Calibration |
| :--- | :--- | :--- |
| **Home Value** | Zillow (ZHVI ZIP-level) | Typical single-family/condo valuation (latest 2026) |
| **Market Rent** | Zillow (ZORI ZIP-level) | Typical observed asking rent (latest 2026) |
| **Property Tax** | Mecklenburg County Assessor | Base county rate ($0.47$) + city municipal levy (ranging from $0.00$ to $0.49$) |
| **State Income Tax** | NC Department of Revenue | Flat $4.5\%$ state individual income tax rate |
| **Demographics** | Census ACS (ZIP-level/ZCTA) | 5-Year population growth, renter ratios, and local poverty rates |
| **School Quality** | NCES & GreatSchools | School performance indexes for the dominant high school feeding the ZIP |
| **Price Volatility** | Zillow historical | 5-year coefficient of variation of home prices |

---

## Scoring Modifications

 We will utilize the same core indices (**Rentability**, **Risk**, and **REOI**), but the min-max normalization cohort boundaries will be calibrated exclusively against the Charlotte ZIP codes rather than the national metros. This ensures a highly sensitive local comparison.

---

## Deliverables

### [Research Outputs]

#### [NEW] [charlotte_zipcode_analysis.md](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/charlotte_zipcode_analysis.md)
The final research paper detailing the sub-market profiles, comparative tables, and scoring results.

#### [NEW] [data/charlotte_zip_raw_data.csv](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/data/charlotte_zip_raw_data.csv)
CSV database containing the aggregated raw metrics for each ZIP code.

#### [NEW] [data/charlotte_zip_scoring_results.csv](file:///c:/Users/mab07/OneDrive/Desktop/RealEstateResearch/data/charlotte_zip_scoring_results.csv)
CSV database containing computed net yields and composite scoring outputs.

---

## Verification Plan

### Manual Verification
- Verify that property tax calculations reflect city vs. county borders (e.g., properties outside the Charlotte city limits, like portions of 28277, pay lower municipal tax rates).
- Cross-reference calculated yields with real-world active listings to check if the cash-flow projections match current property listings.
