# Housing Market Dynamics (2018–2023)
Quantifying how **mortgage rates**, **inflation (CPI)**, and **for-sale inventory** relate to **U.S. home prices**—with city/suburb comparisons and pre/post-COVID breaks.

This repo includes my **Jupyter notebooks**, an **interactive Power BI** report, and a **PDF** with the full write-up.

---

## TL;DR findings

- **2018–2021:** classic negative link—**rates ↓ → prices ↑** (and vice versa) in most markets.  
- **2022–2023:** the link **weakens or flips** in several cities; prices stay high even as rates rise.  
- Patterns line up with **tight inventory** and **CPI spikes**; suburban markets often behave differently from urban cores.

Full narrative, figures, and references: `reports/Data_Analysis_Report.pdf`.

---

## What’s here

- **`notebooks/`** – cleaning, EDA, modeling.  
- **`reports/Data_Analysis_Report.pdf`** – detailed analysis.  
- **`reports/powerbi/HousePrice_vs_InterestRate.pbix`** – interactive dashboard (tracked with Git LFS).  
- **`reports/schedule/HousePriceProject.mpp`** – project timeline (LFS).  

---

## Methodology (what I did)

**Data engineering**
- Standardized mixed CSVs (headers, types, keys), reconciled frequencies, and built a city-month panel.  
- Bounded forward fills for tiny gaps; preserved structural missingness.  
- Created **pre/post-COVID** segments and **rolling windows**.

**Exploratory / statistics**
- Stationarity checks (ADF) where helpful; used levels vs returns as appropriate.  
- **Rolling correlations** between price and rate (12–18m windows) to visualize breaks.  
- Heatmaps and small-multiple trend plots to compare cities and suburbs.


