# Analysis Repository — Technical & Engineering Analyses

## Purpose
The Analysis Repository documents structured analytical investigations, hydraulic evaluations, alternative feasibility assessments, cost-benefit analyses, and engineering calculations. Every entry explicitly distinguishes empirical inputs and grounded evidence from working assumptions, mathematical methods, and analytical conclusions. Assumptions must never be represented as established facts.

---

## Analysis Record Template

```markdown
### Analysis ID: ANL-####
- **Question:** [Specific technical or engineering question addressed]
- **Inputs:** [Input parameters, demand figures, design flows, unit costs]
- **Evidence Used:** [References to specific Claims (CLM-####) and Sources (SRC-####)]
- **Requirements Used:** [References to applicable Requirements (REQ-####)]
- **Assumptions:** [Explicit working assumptions, engineering defaults, safety margins — MUST NOT be stated as established facts]
- **Method:** [Analytical methodology, calculation formula, hydraulic standard, or comparative matrix]
- **Analysis:** [Step-by-step computational or qualitative analysis]
- **Uncertainty:** [Sources of variance, sensitivity, data limitations, or unknown variables]
- **Result:** [Definitive analytical outcome, metric, or recommendation]
- **Review Status:** [DRAFT | QA_CHALLENGED | PE_REVIEWED | APPROVED]
```

---

## Analysis Records

### Analysis ID: ANL-0001
- **Question:** What was the baseline Average Daily Demand (ADD) in Million Gallons per Day (MGD) and the average annual delivery per service connection for the Visalia main water system (CA5410016) during calendar year 2020?
- **Inputs:**
  - Annual water supplied (2020): 30,034 AF (Source: CLM-0001 / SRC-0001 Table 2-1)
  - Active municipal service connections (2020): 45,325 connections (Source: CLM-0001 / SRC-0001 Table 2-1)
  - Calendar days in leap year 2020: 366 days
  - Volumetric conversion constant: 1 Acre-Foot (AF) = 325,851 Gallons
- **Evidence Used:** CLM-0001, CLM-0002, SRC-0001
- **Requirements Used:** REQ-0001 (CWC compliance reporting standards)
- **Assumptions:**
  - Linear volumetric conversion factor of 325,851 gallons per acre-foot.
  - Uniform baseline demand distribution across calendar days (used strictly to derive arithmetic ADD; this working assumption does NOT represent diurnal peaking factors, maximum day demand [MDD], or peak hour demand [PHD]).
  - Gross supplied volume includes non-revenue water/distribution losses, as customer-class billed meter disaggregation is not applied in this initial single-source calculation.
- **Method:**
  1. Total Annual Gallons = 30,034 AF × 325,851 gal/AF = 9,786,608,934 gallons.
  2. Average Daily Demand (ADD) = 9,786,608,934 gallons / 366 days = 26,739,368.67 gal/day = 26.74 MGD.
  3. Average Annual Delivery per Connection = 30,034 AF / 45,325 connections = 0.66263 AF/conn/year ≈ 0.663 AF/conn/year.
  4. Average Daily Delivery per Connection = 26,739,368.67 gal/day / 45,325 connections = 589.95 gal/conn/day ≈ 590 gal/conn/day.
- **Analysis:**
  - The Visalia primary public water system operated at a base production rate of ~26.74 MGD in 2020. Across 45,325 customer accounts, unit gross production averaged ~0.663 AFY per connection (~590 gallons/connection/day). Because 100% of this supply is extracted from the Kaweah Subbasin (CLM-0002), the groundwater production infrastructure must sustain a continuous minimum baseline yield of 26.74 MGD prior to accounting for seasonal summer irrigation peaking or fire flow capacity requirements.
- **Uncertainty:**
  - Metering loss / real distribution leakage is included in gross production and requires AWWA M36 audit reconciliation to determine net customer consumption.
  - Single-year data (2020) was impacted by pandemic residential stay-at-home patterns and drought conditions, which may introduce variance relative to long-term 5-year and 10-year rolling averages.
- **Result:**
  - Baseline 2020 Average Daily Demand (ADD) = 26.74 MGD (30,034 AFY).
  - Average Gross Unit Delivery = 0.663 AF/connection/year (590 gal/connection/day).
- **Review Status:** DRAFT (Preliminary computational synthesis; requires professional engineering verification)
