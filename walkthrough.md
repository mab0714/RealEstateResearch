# Research Walkthrough & Final Deliverables

We have completed the comprehensive real estate, socioeconomic, tax, climate/insurance, and dentist job market relocation research. 

To ensure a pristine, professional repository, we deleted all intermediate draft plans and obsolete python codebase files, reorganizing our final outputs into dedicated folders.

---

## Final Project Structure

```
RealEstateResearch/
├── data/
│   ├── state_taxes.csv                  # State tax rates & dentist market density/salary metrics
│   ├── metro_raw_data.csv               # Raw macro indicators & source vetting URLs
│   ├── metro_scoring_results.csv        # Computed True Net Yields & REOI ranks (Macro)
│   ├── charlotte_zip_raw_data.csv       # Raw Charlotte ZIP code indicators & sources
│   └── charlotte_zip_scoring_results.csv # Calculated ZIP yields, scores, & ranks
├── reports/
│   ├── 1_us_rental_market_analysis.md   # Refined U.S. Macro analysis with insurance-adjusted yields
│   ├── 2_dentist_relocation_analysis.md # Dentist career & real estate investment comparison
│   └── 3_charlotte_zipcode_analysis.md  # Drill-down study of Charlotte ZIP codes
├── task.md                              # Completed phase checklist
└── walkthrough.md                       # This deliverables summary
```

---

## Core Findings Summary

### 1. U.S. Macro Real Estate (Refined with Insurance Drag)
Adjusting our cash-flow model for **actual home insurance premiums** (ranging from $7,136/yr in FL to $2,344/yr in AZ) and **regional CapEx maintenance risks** (foundation cracking in Texas clay soils, hurricane wear in Florida) shifts the cash-flow rankings:
*   **Charlotte, NC (REOI: 61.1 — Rank 1) & Atlanta, GA (REOI: 56.3 — Rank 2):** Rise to the top as they are weather-sheltered markets with low property tax and moderate insurance rates, preserving a strong **2.94% – 2.99% True Net Yield**.
*   **Phoenix, AZ (REOI: 40.7 — Rank 5):** Tied for the second-highest True Net Yield (**2.94%**) due to low property taxes ($0.60\%$) and very low insurance premiums ($2,344/yr).
*   **Miami, FL (REOI: 47.3 — Rank 4) & Tampa, FL (REOI: 20.6 — Rank 8):** Cash flows are heavily eroded by Florida's insurance crisis ($6,500–$7,136/yr premiums), dropping Tampa to Rank 8 (**1.81% True Net Yield**).
*   **Dallas-Fort Worth, TX (REOI: 50.1 — Rank 3):** High property taxes ($1.70\%$) and hail insurance ($4,085/yr) compress net yield to **2.75%**.

### 2. Dentist Relocation Analysis
*   **Texas** is the standout career relocation market. It has the **lowest dentist density in the cohort (25.9 dentists per 100k)**, indicating severe undersaturation and high patient demand, a high average salary (~$207k), and **zero state income tax**.
*   **North Carolina (Charlotte)** is a balanced runner-up, offering strong salaries (~$205k) and Charlotte's Rank 1 real estate opportunity, though it has moderate dentist saturation (~41.7 per 100k) and a flat 4.5% state income tax.

### 3. Charlotte ZIP Code Drill-Down
*   **Steele Creek (28273 — Rank 1):** Top local opportunity ($REOI = 59.1$) combining a $3.19\%$ net yield with high growth ($+11.5\%$) and logistics-driven rental demand.
*   **University City (28269 — Rank 2):** Offers the highest net cash yield (**3.34%**) near the university.
*   **Ballantyne (28277 — Rank 4):** Safest play ($Risk = 0.0$) with top-tier schools and $1.77\%$ net yield.
