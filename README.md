# Pakistan Wheat Deficit Problem Analysis

Data analysis project examining Pakistan's wheat production vs. national demand (2000–2024), and forecasting the yield improvement needed to reach self-sufficiency by 2030.

## Objective

Solve the annual wheat deficit problem in Pakistan by analyzing historical production, population growth, and consumption trends, then projecting what's required to close the supply gap.

## Data Sources

- **Agricultural data**: [Pakistan Agricultural 2000–2024 (FAOSTAT)](https://www.kaggle.com/datasets/azharalisoomro/pakistan-agricultural-20002024-faostat-data) — wheat area harvested, yield, and production.
- **Population data**: [World Population Dataset](https://www.kaggle.com/datasets/azharalisoomro/world-population-dataset) — Pakistan's annual population (World Bank).

## Methodology

1. **Population data prep** — filter for Pakistan, reshape years 2000–2024 into a Year/Population table.
2. **Agricultural data prep** — filter for Wheat, pivot into Area Harvested, Yield, and Production columns per year.
3. **Merge** both datasets on Year into a single working table.
4. **Demand & deficit calculation**:
   - Per-capita wheat consumption benchmark: **125 kg/person/year** (PARC & FAO estimate)
   - +10% overhead for seed reserves, animal feed, and post-harvest losses
   - Deficit/Surplus = Actual Production − Total Demand Required
5. **Visualization** — production vs. demand trend line, and a bar chart of annual shortages.
6. **2030 forecast** — using an estimated population of 268 million, calculates the yield (kg/ha) Pakistan would need to achieve to be self-sufficient, and compares it against the 2024 baseline yield.
7. **Dashboard** — a combined summary view of the current-vs-target yield goal.

## Key Assumptions

| Assumption | Value |
|---|---|
| Per-capita wheat consumption | 125 kg/year |
| Wastage/seed overhead | 10% |
| Estimated 2030 population | 268,000,000 |

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib

## Notebook

`wheat-deficit-problem-analysis.ipynb` — run top to bottom; requires the two CSV datasets above (originally sourced via Kaggle input paths).

## Output

- Historical production vs. demand trend chart
- Annual wheat shortage bar chart
- 2030 required yield vs. current yield comparison
