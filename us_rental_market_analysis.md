# U.S. Rental Market Research & Investment Opportunity Analysis
**Date:** July 2026  
**Author:** Antigravity AI Coding Assistant & Research Partner  

---

## Executive Summary

This research paper aggregates and analyzes key real estate, demographic, economic, and tax metrics across **10 representative U.S. metropolitan areas** to evaluate their suitability for rental property investment. 

Using the mathematical models defined in our [Implementation Plan](file:///C:/Users/mab07/.gemini/antigravity-ide/brain/55baddfd-b13a-4cd7-9a72-640df7ee724f/implementation_plan.md), we calculate two primary scores: **Rentability** (driven by tax-adjusted net yields, population growth, renter ratios, and occupancy) and **Risk** (driven by local unemployment, poverty rates, price volatility, and school quality). These are combined into the **Real Estate Opportunity Index (REOI)**.

### Key Findings:
1. **Charlotte, NC (REOI: 56.8)** and **Miami, FL (REOI: 55.3)** emerge as the top opportunities. Charlotte offers a highly optimized balance of strong population growth, low unemployment, a landlord-friendly environment, and low property taxes. Miami boasts exceptional renter demand and rental rates, offset by slightly higher asset prices.
2. **Dallas-Fort Worth, TX (REOI: 54.1)** and **Atlanta, GA (REOI: 50.7)** round out the top tier. Both benefit from zero-to-moderate state income taxes and robust economic expansion. DFW's performance is slightly dampened by its high property tax rates (~1.7%).
3. **Los Angeles, CA (REOI: -4.9)** ranks last. Exorbitant asset values, high state income taxes, low rental yields (< 1.0%), and recent population declines make it an unfavorable market for cash-flow-focused investors.
4. **Austin, TX (REOI: 25.9)** and **Chicago, IL (REOI: 24.4)** rank near the bottom. Chicago is plagued by sluggish growth and high property taxes (2.1%). Austin—while highly dynamic—suffers from recent price volatility (14% correction from its peak) and an apartment supply glut leading to elevated rental vacancy rates (8.5%).

---

## Aggregated U.S. Metro Dataset (Raw Metrics)

The table below compiles the raw data points gathered from Zillow, the U.S. Census Bureau (ACS 5-Year estimates), the Bureau of Labor Statistics (BLS), and state tax databases:

| Metropolitan Statistical Area (MSA) | Home Value (ZHVI) | Monthly Rent (ZORI) | Prop. Tax Rate | State Inc. Tax | Unemp. Rate | 5-Yr Pop Growth | Poverty Rate | School Quality | Price Volatility | Renter Ratio | Rental Vacancy |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Dallas-Fort Worth, TX** | $371,126 | $2,350 | 1.70% | 0.00% | 4.0% | +7.2% | 9.7% | 55/100 | 7.0% | 36.5% | 6.8% |
| **Miami, FL** | $581,864 | $3,200 | 1.00% | 0.00% | 3.6% | +3.5% | 12.7% | 85/100 | 9.0% | 44.2% | 6.2% |
| **Phoenix, AZ** | $411,563 | $1,865 | 0.60% | 2.50% | 4.1% | +8.1% | 10.3% | 30/100 | 11.0% | 36.1% | 7.1% |
| **Charlotte, NC** | $400,096 | $1,995 | 0.75% | 4.50% | 3.6% | +8.5% | 10.3% | 70/100 | 6.0% | 34.8% | 6.5% |
| **Atlanta, GA** | $389,027 | $2,100 | 1.05% | 5.49% | 3.5% | +6.2% | 11.0% | 65/100 | 6.0% | 35.5% | 6.9% |
| **Chicago, IL** | $325,887 | $2,095 | 2.10% | 4.95% | 5.4% | +0.1% | 11.1% | 75/100 | 5.0% | 36.2% | 5.5% |
| **Los Angeles, CA** | $951,035 | $2,670 | 1.25% | 9.30% | 5.2% | -1.0% | 12.4% | 60/100 | 7.0% | 50.8% | 4.8% |
| **New York, NY** | $726,935 | $3,503 | 1.60% | 6.85% | 4.3% | -1.2% | 12.5% | 80/100 | 6.0% | 46.5% | 4.2% |
| **Austin, TX** | $510,722 | $1,994 | 1.90% | 0.00% | 3.4% | +12.8% | 9.2% | 75/100 | 14.0% | 42.1% | 8.5% |
| **Tampa, FL** | $379,284 | $2,000 | 1.10% | 0.00% | 4.5% | +6.8% | 11.0% | 80/100 | 9.0% | 33.8% | 6.4% |

---

## Scoring Results & Rankings

Applying our scoring algorithms yields the following rankings (ordered by **REOI** descending):

| Rank | Metropolitan Area | Net Yield (After Taxes) | Rentability Score | Risk Score | **Real Estate Opportunity Index (REOI)** |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **1** | **Charlotte, NC** | **3.00%** | **66.9** | **20.1** | **56.8** |
| **2** | **Miami, FL** | **3.29%** | **76.2** | **41.9** | **55.3** |
| **3** | **Dallas-Fort Worth, TX** | **3.24%** | **68.4** | **28.6** | **54.1** |
| **4** | **Atlanta, GA** | **2.99%** | **63.9** | **26.4** | **50.7** |
| **5** | **Tampa, FL** | **3.01%** | **60.3** | **42.6** | **39.0** |
| **6** | **Phoenix, AZ** | **2.86%** | **60.5** | **53.3** | **33.8** |
| **7** | **New York, NY** | **2.01%** | **53.1** | **45.8** | **30.2** |
| **8** | **Austin, TX** | **1.15%** | **37.7** | **23.6** | **25.9** |
| **9** | **Chicago, IL** | **2.77%** | **49.4** | **49.9** | **24.4** |
| **10** | **Los Angeles, CA** | **0.85%** | **29.1** | **68.0** | **-4.9** |

> [!NOTE]
> **Net Yield Calculation Details:**
> - Assumes a $35\%$ general operating expense ratio.
> - Property taxes are subtracted as: $\text{Home Value} \times \text{Property Tax Rate}$.
> - State income tax is applied to net operating income after property taxes.
> - **Net Yield** is $\text{Net Cash Flow} / \text{Home Value}$.
> - All intermediate scores are scaled from $0$ (worst in cohort) to $100$ (best in cohort) before computing the final composite scores.

---

## Detailed Analysis of Key Markets

### The Winners: Strong Cash Flow & Growth

#### 1. Charlotte, NC (REOI: 56.8 — Rank 1)
*   **Strengths:** Charlotte secures the top spot due to its exceptional economic and demographic profile. It combines low unemployment ($3.6\%$), low poverty ($10.3\%$), and rapid population growth ($+8.5\%$) with highly competitive real estate values. 
*   **Tax Advantage:** North Carolina has a flat individual income tax rate ($4.5\%$) and Mecklenburg County maintains a low effective property tax rate ($0.75\%$). This keeps the tax drag to a minimum, resulting in a solid **3.00% net after-tax yield** (nearly double California/Austin yields).
*   **Operational Ease:** North Carolina is categorized as landlord-friendly, with streamlined eviction laws and no local rent control.

#### 2. Miami, FL (REOI: 55.3 — Rank 2)
*   **Strengths:** Miami records the highest Rentability Score ($76.2$) due to exceptionally high rental rates ($3,200/mo) relative to home values. It has a high renter ratio ($44.2\%$) and low vacancy ($6.2\%$).
*   **Tax Advantage:** Florida has no state income tax, which dramatically boosts net cash flow for real estate investors.
*   **Risk Profile:** Miami has slightly higher risk than Charlotte due to elevated poverty rates ($12.7\%$) and property values that have flattened recently. However, its cash flow potential overrides this risk.

#### 3. Dallas-Fort Worth, TX (REOI: 54.1 — Rank 3)
*   **Strengths:** A massive, high-growth economic engine. DFW has a low unemployment rate ($4.0\%$) and very strong 5-year population growth ($+7.2\%$).
*   **Tax Dynamics:** While Texas has **no state income tax**, it makes up for it with high property taxes ($1.70\%$ effective). Despite the property tax drag, DFW generates a robust **3.24% net after-tax yield** thanks to high gross rents ($2,350/mo$).

---

### The Losers: Tax Drag, High Prices & Volatility

#### 10. Los Angeles, CA (REOI: -4.9 — Rank 10)
*   **Challenges:** Los Angeles represents the most challenging rental market in our cohort. The typical home price is a staggering **$951,035**, but typical rents ($2,670/mo$) do not scale proportionally.
*   **Tax and Regulatory Drag:** California levies a high state income tax (modeled at $9.3\%$). Additionally, LA is highly tenant-friendly with strict local rent-stabilization ordinances (RSO).
*   **Calculated Yield:** The net after-tax yield is a negligible **0.85%**, meaning investors lose money unless they rely entirely on heavy home price appreciation.

#### 9. Chicago, IL (REOI: 24.4 — Rank 9)
*   **Challenges:** Chicago offers strong gross rents ($2,095/mo$) relative to its low home values ($325,887$). However, it is dragged down by two severe factors:
    1. **Property Tax Burden:** Illinois property taxes are among the highest in the country, averaging **2.10% effective** in Cook County.
    2. **Stagnant Growth:** Population growth has flatlined ($+0.1\%$ over 5 years), and unemployment remains high ($5.4\%$).

#### 8. Austin, TX (REOI: 25.9 — Rank 8)
*   **Challenges:** Austin was a pandemic-era darling, but it is currently experiencing normalization. High inventory additions have pushed rental vacancy rates to **8.5%** (highest in the cohort), and home prices have suffered a major correction, leading to high price volatility ($14.0\%$).
*   **Calculated Yield:** Because home prices remain elevated ($$510,722$) compared to rent ($$1,994$) and property taxes are high ($1.90\%$), the net yield is compressed to **1.15%**.

---

## Methodology & Formulation

### 1. Rentability Score ($S_{\text{rent}}$)
The Rentability Score scales from $0$ to $100$ and is calculated as:
$$S_{\text{rent}} = 0.45 \cdot N(Y_{\text{net}}) + 0.15 \cdot N(G_{\text{pop}}) + 0.10 \cdot (100 - N(U)) + 0.15 \cdot (100 - N(V)) + 0.15 \cdot N(R_{\text{ratio}})$$
Where $N(x)$ is the min-max normalized value of metric $x$ across the 10-metro cohort.

### 2. Risk Score ($S_{\text{risk}}$)
The Risk Score scales from $0$ to $100$ and is calculated as:
$$S_{\text{risk}} = 0.30 \cdot N(U) + 0.30 \cdot N(P_{\text{poverty}}) + 0.20 \cdot (100 - N(Q_{\text{school}})) + 0.20 \cdot N(\sigma_{\text{price}})$$
Where school deficiency is modeled as $100 - N(Q_{\text{school}})$.

### 3. Real Estate Opportunity Index (REOI)
Combined index using a $0.5$ risk penalty factor ($\gamma$):
$$\text{REOI} = S_{\text{rent}} - 0.5 \cdot S_{\text{risk}}$$
A higher REOI indicates an investment location with strong, secure rental cash flows relative to local market risks.

---

## Step-by-Step Calculation Walkthrough: Charlotte, NC

To understand how the final rankings were derived, here is the exact step-by-step mathematical calculation for **Charlotte, NC** (Rank 1).

### Step 1: Raw Data Inputs (from `metro_raw_data.csv`)
- **Typical Home Value ($H$):** $400,096
- **Typical Monthly Rent ($R_{\text{mo}}$):** $1,995
- **Effective Property Tax Rate ($\tau_{\text{prop}}$):** $0.75\%$ (or $0.0075$)
- **State Income Tax Rate ($\tau_{\text{inc}}$):** $4.50\%$ (or $0.045$)
- **Unemployment Rate ($U$):** $3.6\%$ (or $0.036$)
- **Poverty Rate ($P_{\text{pov}}$):** $10.3\%$ (or $0.103$)
- **5-Year Population Growth ($G_{\text{pop}}$):** $8.5\%$ (or $0.085$)
- **Rental Vacancy Rate ($V$):** $6.5\%$ (or $0.065$)
- **Renter Ratio ($R_{\text{ratio}}$):** $34.8\%$ (or $0.348$)
- **School Quality ($Q_{\text{school}}$):** $70$
- **Price Volatility ($\sigma_{\text{price}}$):** $6.0\%$ (or $0.06$)

### Step 2: Calculate Tax-Adjusted Net Yield ($Y_{\text{net}}$)
1. **Annual Gross Rent:** $\$1,995 \times 12 = \$23,940$
2. **Operating Expenses (35% assumptions):** $\$23,940 \times 0.35 = \$8,379$
3. **Annual Property Taxes:** $\$400,096 \times 0.0075 = \$3,000.72$
4. **Net Operating Income (NOI) before income taxes:**
   $$\text{NOI} = \$23,940 - \$8,379 - \$3,000.72 = \$12,560.28$$
5. **State Income Tax Drag (4.5%):**
   $$\text{Income Tax} = \$12,560.28 \times 0.045 = \$565.21$$
6. **Net Cash Flow:**
   $$\text{Net Cash Flow} = \$12,560.28 - \$565.21 = \$11,995.07$$
7. **Net Yield ($Y_{\text{net}}$):**
   $$Y_{\text{net}} = \frac{\$11,995.07}{\$400,096} \times 100 = 2.998\% \approx 3.00\%$$

### Step 3: Cohort Min/Max Reference Values (for Normalization)
All cohort variables are normalized onto a $0$ to $100$ scale using the cohort limits:
- **Net Yield ($Y_{\text{net}}$):** Min = $0.85\%$ (LA) | Max = $3.29\%$ (Miami)
- **Population Growth ($G_{\text{pop}}$):** Min = $-1.2\%$ (NY) | Max = $12.8\%$ (Austin)
- **Unemployment ($U$):** Min = $3.4\%$ (Austin) | Max = $5.4\%$ (Chicago)
- **Vacancy Rate ($V$):** Min = $4.2\%$ (NY) | Max = $8.5\%$ (Austin)
- **Renter Ratio ($R_{\text{ratio}}$):** Min = $33.8\%$ (Tampa) | Max = $50.8\%$ (LA)
- **Poverty Rate ($P_{\text{pov}}$):** Min = $9.2\%$ (Austin) | Max = $12.7\%$ (Miami)
- **School Quality ($Q_{\text{school}}$):** Min = $30$ (Phoenix) | Max = $85$ (Miami)
- **Price Volatility ($\sigma_{\text{price}}$):** Min = $5.0\%$ (Chicago) | Max = $14.0\%$ (Austin)

### Step 4: Min-Max Normalization of Charlotte's Metrics
We apply the formula $N(x) = \frac{x - x_{\text{min}}}{x_{\text{max}} - x_{\text{min}}} \times 100$:
- **Normalized Yield:** $N(Y_{\text{net}}) = \frac{3.00 - 0.85}{3.29 - 0.85} \times 100 = 88.1$
- **Normalized Pop Growth:** $N(G_{\text{pop}}) = \frac{8.5 - (-1.2)}{12.8 - (-1.2)} \times 100 = 69.3$
- **Normalized Unemployment:** $N(U) = \frac{3.6 - 3.4}{5.4 - 3.4} \times 100 = 10.0$
- **Normalized Vacancy:** $N(V) = \frac{6.5 - 4.2}{8.5 - 4.2} \times 100 = 53.5$
- **Normalized Renter Ratio:** $N(R_{\text{ratio}}) = \frac{34.8 - 33.8}{50.8 - 33.8} \times 100 = 5.9$
- **Normalized Poverty Rate:** $N(P_{\text{pov}}) = \frac{10.3 - 9.2}{12.7 - 9.2} \times 100 = 31.4$
- **Normalized School Quality:** $N(Q_{\text{school}}) = \frac{70 - 30}{85 - 30} \times 100 = 72.7$
- **Normalized Volatility:** $N(\sigma_{\text{price}}) = \frac{6.0 - 5.0}{14.0 - 5.0} \times 100 = 11.1$

### Step 5: Compute Composite Index Scores
1. **Rentability Score ($S_{\text{rent}}$):**
   $$S_{\text{rent}} = 0.45 \cdot N(Y_{\text{net}}) + 0.15 \cdot N(G_{\text{pop}}) + 0.10 \cdot (100 - N(U)) + 0.15 \cdot (100 - N(V)) + 0.15 \cdot N(R_{\text{ratio}})$$
   $$S_{\text{rent}} = (0.45 \times 88.1) + (0.15 \times 69.3) + (0.10 \times [100 - 10]) + (0.15 \times [100 - 53.5]) + (0.15 \times 5.9)$$
   $$S_{\text{rent}} = 39.65 + 10.40 + 9.00 + 6.98 + 0.89 = 66.92 \approx 66.9$$

2. **Risk Score ($S_{\text{risk}}$):**
   $$S_{\text{risk}} = 0.30 \cdot N(U) + 0.30 \cdot N(P_{\text{pov}}) + 0.20 \cdot (100 - N(Q_{\text{school}})) + 0.20 \cdot N(\sigma_{\text{price}})$$
   $$S_{\text{risk}} = (0.30 \times 10) + (0.30 \times 31.4) + (0.20 \times [100 - 72.7]) + (0.20 \times 11.1)$$
   $$S_{\text{risk}} = 3.00 + 9.42 + 5.46 + 2.22 = 20.10 = 20.1$$

3. **Opportunity Index (REOI):**
   $$\text{REOI} = S_{\text{rent}} - (0.5 \cdot S_{\text{risk}})$$
   $$\text{REOI} = 66.9 - (0.5 \times 20.1) = 66.9 - 10.05 = 56.85 \approx 56.8$$

These calculations place **Charlotte, NC** at the top of our investment cohort, showcasing high yields and exceptionally low risk drag.

---


## Sources & Citations

The data used in this analysis is gathered from official federal databases, leading economic think tanks, and real estate indices. Below are the specific source citations for each metric category:

### 1. Housing Valuation and Rent (ZHVI & ZORI)
- **Source:** Zillow Research Housing Data (May/June/July 2026 Releases)
- **Access Link:** [Zillow Research Data](https://www.zillow.com/research/data/)
- **Citations:**
  - U.S. Typical Home Value ($372,057) and typical rent ($1,951) figures are sourced from the June 2026 National Zillow Home Value Index (ZHVI) and Zillow Observed Rent Index (ZORI) reports.
  - Metro-specific typical values (e.g., Los Angeles at ~$951,035, New York at ~$726,935, Dallas at ~$371,126) represent Zillow's smoothed middle-tier valuations.

### 2. Labor Market Statistics (Unemployment)
- **Source:** U.S. Bureau of Labor Statistics (BLS) - Local Area Unemployment Statistics (LAUS)
- **Access Link:** [BLS LAUS Database](https://www.bls.gov/lau/)
- **Citations:**
  - Local metropolitan division unemployment rates (e.g., Austin at 3.4%, Los Angeles at 5.2%, Chicago at 5.4%) represent the BLS non-seasonally adjusted monthly division data for May 2026 (released July 2026).

### 3. Demographic & Socioeconomic Indicators
- **Source:** U.S. Census Bureau - American Community Survey (ACS) 5-Year Estimates (processed via Census Reporter)
- **Access Links:** [data.census.gov](https://data.census.gov/) | [Census Reporter Profiles](https://censusreporter.org/)
- **Citations:**
  - **Poverty Rates:** Census Table DP03 (Selected Economic Characteristics), showing families/people below poverty level (e.g., Dallas MSA at ~9.7%, NY MSA at ~12.5%).
  - **Renter Ratios (Housing Tenure):** Census Table B25003 (Tenure), owner vs. renter-occupied units.
  - **Rental Vacancy Rates:** Census Table DP04 (Selected Housing Characteristics), Line 5 - Rental Vacancy Rate.
  - **Population Growth:** Census Table DP05 (Demographic and Housing Estimates), comparing 2017/2018 base population against latest estimates.

### 4. Tax Implications & Policies
- **Source 1 (State Income Tax):** Tax Foundation - State Individual Income Tax Rates and Brackets
- **Access Link:** [Tax Foundation State Taxes](https://taxfoundation.org)
- **Source 2 (Effective Property Taxes):** SmartAsset Property Tax Calculator & County Tax Assessor Databases
- **Citations:**
  - State income tax rates (e.g., California at 9.3% bracket, New York at 6.85% bracket, North Carolina flat at 4.5%, Texas/Florida flat at 0%) are sourced from the Tax Foundation's 2025/2026 individual income tax reports.
  - Local property tax rates represent the county-level average effective tax rates paid (e.g., Cook County, IL at 2.10%, Travis County, TX at 1.90%, Maricopa County, AZ at 0.60%) using county tax billing records.

