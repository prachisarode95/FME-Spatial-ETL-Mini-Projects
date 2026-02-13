# Leverage Ordered Data – FME Form Advanced

## Project Overview  
This project focuses on using ordered datasets to perform calculations across sequential records in FME. The goal is to demonstrate how to compute monthly differences in precipitation values using record ordering and attribute transformation. This simulates real-world scenarios such as time series comparison, trend analysis, and delta generation from ordered tabular data.

---

## Core Tools Used  
- **AttributeManager** – Performs attribute-level math to compute the difference between precipitation values of adjacent months  
- **Excel Reader/Writer (XLSXR/XLSXW)** – Reads raw monthly precipitation from a spreadsheet and writes enriched output  
- **Visual Preview** – Validates in-line record results before writing to file

---

## Inputs & Outputs  

| Input File | Output File |
|------------|-------------|
| `Precipitation.xlsx` (Month, Precipitation) | `Precipitation_Processed.xlsx` (Month, Precipitation, MonthlyPrecipitation) |

Example Output:

| Month | Precipitation | MonthlyPrecipitation |
|-------|----------------|----------------------|
| Jan   | 168            | 168                  |
| Feb   | 273            | 105                  |
| Mar   | 387            | 114                  |
| Apr   | 476            | 89                   |

---

## Workflow Highlights  

1. **Read Input Table**: The Excel file is read as a sequential table containing months and raw precipitation.
2. **Calculate Differences**: `AttributeManager` computes the month-on-month delta by subtracting previous row values (simulating a running difference).
3. **Write Clean Output**: Final output is saved into a clean Excel format with the newly computed field.
4. **Visual Validation**: Output is reviewed using Visual Preview to confirm correct calculations before export.

---

## Key Takeaway  
This mini-project highlights your ability to perform **record-wise arithmetic on sequential datasets** using FME. It’s especially useful for automation pipelines that require:
- Monthly or temporal comparisons  
- Stock or rainfall trend deltas  
- Attribute change summaries based on sequence

---

*Workspace Screenshot*:

![Workspace](https://github.com/user-attachments/assets/d13933df-7eaf-43bd-a65f-5badba9257a7)

---

> This project demonstrates clear command over attribute-based transformations, ordered data logic, and streamlined Excel ETL—ideal for time series workflows in domains like weather, finance, or infrastructure reporting.
