# imf-sdr-loans-processing
Scripts to download and convert IMF country-level loan data into clean CSV files.
# IMF Country-Level Loan Data (SDRs)

This repository contains scripts to download, clean, and organize IMF country-level loan data denominated in Special Drawing Rights (SDRs), and to export the data into clean CSV files ready for analysis.

The scripts focus on data acquisition and formatting only. No currency conversion or analytical transformations are performed in this repository.

---

## Data Source

The data are obtained directly from the International Monetary Fund (IMF) website:

- **IMF loan actuals** (monthly, country-level)  
  IMF `extrep2` tables
- **IMF loan projections** (country-level repayment schedules)  
  IMF `extfor2` tables

All monetary values are reported by the IMF in **millions of SDRs**.

---

## What the Scripts Do

The scripts in this repository:

1. Download IMF loan tables from the IMF website
2. Parse and clean the raw table structure
3. Organize the data at the **country level**
4. Export clean CSV files for further use

The outputs include:
- Monthly country-level loan actuals
- Country-level loan projections aggregated over specified periods

---

## Output Files

The processed data are saved as CSV files and can be used directly in downstream analysis or merged with other datasets.

Typical outputs include:
- Monthly country-level actual loan flows
- Country-level projected loan totals over a specified period

---

## Scope and Limitations

- This repository **does not perform currency conversion** (e.g. SDR to USD).
- It does not include economic analysis or modeling.
- The purpose of the repository is strictly **data collection and preparation**.

---

## Requirements

- Python 3
- pandas
- requests

Some scripts may require additional packages depending on the file formats used (e.g. `xlrd` for legacy `.xls` files).

---

## Notes

The scripts were written to ensure transparency and reproducibility in the construction of IMF loan datasets. They can be adapted or extended for other IMF reporting periods or similar data sources.
