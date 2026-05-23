# EPA Hazardous Waste Biennial Report Analysis | 2021 vs. 2023

## Project Overview
This project analyzes EPA Hazardous Waste Biennial Report (BR) data to measure how hazardous waste generation in the United States changed between 2021 and 2023. Using Python to process 3.6 million rows of facility-level reporting data, the analysis identifies national trends, top generating facilities, industry-level shifts, waste type composition, and the specific state-waste code combinations driving the largest changes.

**Tools Used:** Python (Pandas, NumPy), Tableau  
**Skills Demonstrated:** Large dataset processing, aggregation, pivot tables, cohort comparison, concentration analysis, cumulative share calculation, CSV export for visualization  
**Dashboard:** [View on Tableau Public](https://public.tableau.com/app/profile/andrew.wilding/viz/BRReporting/WasteCodeDashboard)

---

## Dataset
**Source:** [EPA RCRA Hazardous Waste Biennial Report](https://rcrapublic.epa.gov/rcra-hwip/data-access/csv-downloads)  
The Biennial Report is required under Sections 3002 and 3004 of the Resource Conservation and Recovery Act (RCRA). It covers hazardous waste generated, managed, shipped, and received by large quantity generators and treatment, storage, and disposal facilities.

| Year | Rows | Total Tons Generated |
|---|---|---|
| 2021 | 1,829,496 | 82,368,244 |
| 2023 | 1,769,356 | 69,684,726 |
| **Combined** | **3,598,852** | — |

> Note: The CSV files are too large for GitHub. They can be downloaded from the EPA directly:  
> [BR_REPORTING_2021.zip (40.81 MB)](https://rcrapublic.epa.gov/rcra-hwip/data-access/csv-downloads)  
> [BR_REPORTING_2023.zip (41.17 MB)](https://rcrapublic.epa.gov/rcra-hwip/data-access/csv-downloads)

---

## Key Findings

### National Totals
Total hazardous waste generation fell by **12.7 million tons (-15.4%)** from 2021 to 2023. This is a substantial national reduction across a two-year reporting cycle.

### Facility Concentration
Hazardous waste generation is highly concentrated among a small number of large facilities:
- The **top 20 facilities** accounted for **67.0% of all waste generated in 2023**
- That share was even higher in 2021 at 70.9%, suggesting the industry is becoming slightly less concentrated
- The single largest generator in 2023 was **MPM Silicones LLC (New York)** at 6.58 million tons — 9.4% of the national total

### Biggest Change: MPM Silicones
The largest driver of the national decline was MPM Silicones LLC, which fell from **14.3 million tons in 2021 to 6.6 million tons in 2023** — a reduction of 7.75 million tons (-54.1%). This single facility accounts for more than half of the entire national decrease.

### State-Level Highlights
| State | 2021 Tons | 2023 Tons | Change |
|---|---|---|---|
| New York | 27,118,682 | 19,881,003 | -26.7% |
| Texas | 30,988,747 | 27,894,005 | -10.0% |
| California | 425,720 | 778,752 | +82.9% |
| New Mexico | 3,820 | 771,741 | +20,103% |
| Washington | 114,290 | 263,308 | +130.4% |

New York's dramatic decline is almost entirely attributable to MPM Silicones. New Mexico and Washington show large percentage increases from low baselines.

### Industry Trends (NAICS)
The plastic resins industry (NAICS 325211) saw the steepest decline, dropping **9.4 million tons (-58.1%)**, again largely driven by MPM Silicones. Petroleum refineries (324110) declined 18.1%. Meanwhile, electric power generation (221112) grew by over 3,200%, though from a very small base.

### Waste Code Composition
F039 (multi-source leachate) remains the largest waste code group at 24.2 million tons, representing 35.0% of 2023 generation — up from 29.5% in 2021 as other categories declined faster. D002 (corrosive waste) saw the largest absolute decrease, falling 7.3 million tons (-58.2%).

---

## Analysis Sections
| Section | Description |
|---|---|
| National Totals | Year-over-year change in total tons and record count |
| State Totals | State-level breakdown with delta and percentage change |
| Facility Concentration | Top 20 generators, national share, cumulative share |
| Persistent Top Facilities | Facilities appearing in top 20 in both years |
| Industry (NAICS) Analysis | Waste generation by industry with composition share |
| Waste Code Analysis | Breakdown by waste code group with change metrics |
| Drivers of Change | Top state × waste code combinations driving increases and decreases |

---

## Files
| File | Description |
|---|---|
| `BR_Project.ipynb` | Full analysis notebook with all sections and outputs |
| `CSVs for Visualization/` | Exported CSVs used to build the Tableau dashboard |
