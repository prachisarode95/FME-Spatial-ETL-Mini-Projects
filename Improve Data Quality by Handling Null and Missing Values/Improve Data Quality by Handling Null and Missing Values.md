# Improve Data Quality by Handling Null and Missing Values – FME Form Advanced

## Project Overview  
This project focuses on enhancing data quality by identifying and correcting missing or null attribute values in a parks dataset. The goal is to ensure consistent, usable information across all features by assigning default values, sorting, and aligning fields before final export. These are common preprocessing tasks required before spatial analysis, visualization, or reporting.

---

## Core Tools Used  
- **NullAttributeMapper** – Fills in missing values using rules or fallback fields  
- **Sorter** – Organizes features based on `ParkId` for consistency and downstream control  
- **Visual Preview** – Used to validate clean, complete tabular output  
- **MITAB Reader** and **File Geodatabase Writer (FGDB)** – Reads raw park data and writes cleaned output to GDB

---

## Inputs & Outputs  

| Input Format | Output Format |
|--------------|----------------|
| MapInfo TAB (Parks with nulls) | File Geodatabase (.gdb) – Fully populated attributes |

Example Fields Handled:
- `ParkId`  
- `ParkName`  
- `NeighborhoodName`  
- `VisitorCount`, `Washrooms`, `SpecialFeatures`

---

## Workflow Highlights  

1. **Read Raw Data**: Ingest a MapInfo TAB file with various missing fields.
2. **Map Null Attributes**: Use two `NullAttributeMapper` transformers to assign fallback values:
   - First mapper standardizes primary fields (e.g., `VisitorCount`)
   - Second mapper handles display-friendly names (e.g., `ParkName`, `NeighborhoodName`)
3. **Sort & Structure**: Apply `Sorter` to order rows by `ParkId` for consistency.
4. **Write Clean Output**: Export as a structured File Geodatabase table.

---

*Workspace Screenshot*:

![Workspace Screenshot](https://github.com/user-attachments/assets/0b7f73d4-2469-4db5-8097-c3c1bb9318ae)

---

> This project highlights the ability to automate missing value handling and enforce schema consistency—key skills for preparing reliable data inputs for dashboards, spatial analysis, and database updates. It demonstrates confidence in managing real-world datasets with nulls and producing clean, enterprise-ready outputs like File GDB.
