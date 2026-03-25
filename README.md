# Global Economic Trends: GDP Growth vs. Unemployment Analysis

**Data Visualization Final Project** | Siddartha Bandi

---

## Overview

This project analyzes the relationship between **GDP growth** and **unemployment rates** across countries globally, spanning data from **1921 to 2023**. Using data sourced from the International Monetary Fund (IMF) and global unemployment datasets, the project transforms raw economic indicators into clean, analysis-ready formats and builds interactive **Tableau dashboards** to visualize long-term trends, country comparisons, and the correlation between economic output and labor markets.

---

## Data Sources

| File | Source | Description |
|------|--------|-------------|
| `IMF.xls` | International Monetary Fund | Government expenditure and GDP growth data |
| `gdp_1921-2023.csv` | IMF (processed) | Melted GDP growth data by country and year (1921–2023) |
| `unemployment_transformed.csv` | Global unemployment dataset (processed) | Melted unemployment rate (%) by country and year |

---

## Methodology

### Data Wrangling (`DV.ipynb`)
1. **Unemployment Data Transformation**
   - Loaded raw wide-format Excel data
   - Replaced missing values (`'no data'` → `'Nil'`)
   - Melted from wide to long format: `Country`, `Year`, `Unemployment Rate (%)`
   - Exported as `unemployment_transformed.csv`

2. **GDP Data Transformation**
   - Loaded IMF Excel file with GDP growth by country/year
   - Dropped irrelevant columns interactively
   - Melted to long format: `Year`, `GDP Growth`
   - Filtered out null entries
   - Exported as `gdp_1921-2023.csv`

### Visualization (Tableau)
- Built interactive dashboards in **Tableau** using the processed datasets
- Visualizations include: time-series GDP trends, unemployment rate heatmaps by country, and GDP vs. unemployment scatter correlations
- Published as both `.twb` (Tableau workbook) and `.twbx` (packaged with data)

---

## Repository Contents

```
Final Project/
├── README.md
├── DV.ipynb                                         # Python data wrangling notebook
├── gdp_1921-2023.csv                               # Processed GDP growth dataset
├── unemployment_transformed.csv                    # Processed unemployment dataset
├── IMF.xls                                          # Raw IMF source data
├── SiddarthaBandi_Global Economic Trends.twb        # Tableau workbook
├── SiddarthaBandi.twbx                             # Tableau packaged workbook
├── SiddarthaBandi_Global Economic Trends.pdf       # Final written report
├── Global Economic Trends.docx                     # Report (Word format)
└── GDP vs Unemployment_Siddartha Bandi.pptx        # Presentation slides
```

---

## Key Findings

- Long-run GDP growth shows significant volatility during major economic events (Great Depression, WWII, 2008 Financial Crisis, COVID-19)
- Unemployment rates exhibit a lagged inverse relationship with GDP growth — recessions cause unemployment spikes 1–2 years after GDP contraction
- Developed economies show tighter GDP-unemployment correlations compared to developing nations
- Post-2008 recovery patterns differ substantially between regions (Europe vs. North America vs. Asia)

---

## Setup & Usage

### Python (Data Processing)
```bash
pip install pandas openpyxl
```
Open `DV.ipynb` in Jupyter or Google Colab and run cells sequentially to reproduce the transformed CSV files.

### Tableau (Visualization)
1. Open `SiddarthaBandi_Global Economic Trends.twb` or `SiddarthaBandi.twbx` in **Tableau Desktop**
2. Ensure `gdp_1921-2023.csv` and `unemployment_transformed.csv` are in the same directory as the `.twb` file
3. Explore dashboards interactively

---

## Technologies Used

| Category | Tools |
|----------|-------|
| Language | Python 3.x |
| Data Processing | Pandas, openpyxl |
| Visualization | Tableau Desktop |
| Data Sources | IMF, Global Unemployment Database |
| Environment | Google Colab, Tableau Public |

---

## Author

**Siddartha Bandi**
Data Visualization — Final Project
