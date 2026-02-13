# Utilize Advanced User Parameter Techniques – FME Form Advanced

## Project Overview

This mini-project explores how to incorporate **advanced user parameter techniques** in an FME workspace. By combining **conditional logic**, **statistical computation**, and **custom labeling**, the workflow dynamically filters, analyzes, and outputs park data with precision. This exercise demonstrates how to enhance interactivity, logging, and control in a user-facing data pipeline.

---

## Core Tools Used

* **MITAB Reader/Writer** – To read/write spatial park datasets
* **AttributeManager** – For attribute renaming and restructuring
* **Tester** – Applies user-defined rules to filter records
* **AreaCalculator** – Computes polygonal area
* **StatisticsCalculator** – Aggregates area statistics
* **LabelPointReplacer** – Creates label points for output
* **Creator** – Generates metadata logs
* **Advanced User Parameters** – Enable dynamic control over test conditions, labeling, and outputs

---

## Inputs & Outputs

| Input Dataset                | Output Format |
| ---------------------------- | ------------- |
| `Parks.tab`                  | → `ParksMaintenanceData.tab` |
|                              | → `ParkLabels.tab`           |
|                              | → `TranslationLog.tab`       |

Example:

* Input: Park dataset with fields like `TreeCount`, `DogPark`, `VisitorCount`
* Output:

  * Filtered parks with maintenance and area stats
  * Label points for cartographic display
  * Translation log documenting run metadata

---

## Workflow Highlights

1. **Filter Parks by Criteria** using a Tester transformer with user-defined rules (e.g., tree or visitor thresholds).
2. **Calculate Park Area** and use a StatisticsCalculator to summarize results.
3. **Write Cleaned Data** to maintenance tables and labeled outputs.
4. **Parameter-Driven Logic** enables flexible adjustments to park filtering, logging, and labeling.
5. **Auto-generate Translation Log** for traceability using Creator transformer.

---

## Key Takeaway

This project highlights how **advanced user parameters and dynamic testing logic** can enhance FME workflows with interactivity, adaptability, and transparency. Such techniques are invaluable in production environments where users need to control what data passes through, and where traceability is critical.

---

*Workspace Screenshot*:

![Workspace Screenshot](https://github.com/user-attachments/assets/a0faec9c-decc-475c-ab77-e1f928a3092e)

---

> This project showcases dynamic data filtering, user-driven parameter logic, and logging—all key for creating intelligent, reusable FME workflows.
