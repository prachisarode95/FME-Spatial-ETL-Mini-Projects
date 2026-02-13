# Read from and Write to Multiple Locations (Fanouts) – FME Form Advanced

## Project Overview  
This mini-project demonstrates how to use **fanouts** in FME to dynamically write features into multiple outputs based on attribute values. Fanouts help automate the separation of datasets by category, location, or feature type, without the need for manual creation of separate writers. This is essential for scalable, multi-target data distribution.

---

## Core Tools Used  
- **Generic Reader (FileGDB)** – Reads a complex File Geodatabase dataset  
- **Generic Writer (using Fanouts)** – Writes data to multiple output files or datasets based on attribute logic  
- **Published Parameters** – Enable dynamic output folder selection  
- **Fanout by Attribute** – Automatically creates multiple destination files (e.g., one per vendor, zone, or feature type)

---

## Inputs & Outputs  

| Input Dataset | Output Format |
|---------------|----------------|
| File Geodatabase with various civic assets | Multiple fanout GDBs or folders, separated by `fme_feature_type` or custom attributes |

Example:
- Input: One dataset with all assets (parks, libraries, fountains)
- Output: Separate files or folders for each feature type (e.g., `Libraries.gdb`, `Parks.gdb`, `Fountains.gdb`)

---

## Workflow Highlights  

1. **Data Ingestion**: Load a single complex geodatabase containing multiple feature types.
2. **Fanout Logic Setup**: Configure writer fanouts based on `fme_feature_type` or any relevant attribute.
3. **Dynamic Output Control**: Use published parameters to control the base output path or schema.
4. **Write to Multiple Targets**: FME automatically separates and writes each category to its respective destination without requiring duplicate writers.

---

## Key Takeaway  
This project highlights the power of **dynamic, scalable writing in FME**. Fanouts remove the need for repetitive configuration and allow one workspace to support unlimited feature classes, client zones, or regions. It prepares you for **real-world enterprise workflows where data must be delivered to multiple systems, departments, or files** in a repeatable way.

---

*Workspace Screenshot*:

![Workspace Screenshot](https://github.com/user-attachments/assets/91b4e0be-3c6f-47a8-ae1a-10dc248f635c)

---

> This project showcases efficient, scalable data delivery using dynamic fanouts. It reflects strong automation skills for managing multi-output workflows within a single workspace—ideal for enterprise ETL tasks like client reporting, zone-wise exports, and cloud-based GIS pipelines. A key capability for roles in GIS automation, urban data management, and spatial data engineering.
