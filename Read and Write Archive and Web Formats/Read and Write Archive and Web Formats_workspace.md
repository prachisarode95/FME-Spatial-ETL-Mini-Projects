# Read & Write Archive and Web-Based Formats – FME Form Advanced

## Project Overview  
This project demonstrates how to automate the reading and writing of spatial data from both compressed archives and web-based services using FME Form 2024. The goal is to ingest, transform, style, and upload datasets dynamically using a combination of database joins, KML formatting, string replacement, and FME Flow integration.

---

## Core Tools Used  
- **DatabaseJoiner** – Joins tabular data with spatial features  
- **KMLStyler** – Styles features for KML output based on defined attributes  
- **FeatureWriter** – Writes the transformed data to a structured output  
- **StringReplacer** – Updates attribute text based on rules  
- **FMEFlowResourceConnector** – Publishes the final result to an FME Flow destination (e.g., web portal or shared resource)

---

## Inputs & Outputs  

| Input Source | Output Destination |
|--------------|--------------------|
| ZIP archive with road network | Styled KML File with Snowfall Predictions  
| Web-based attribute data (via DB join) | Published to FME Flow resource repository  
| Structured string attributes | Cleaned and replaced before upload |

---

## Workflow Highlights  

1. **Data Ingestion**: Reads from a pre-extracted archive containing spatial features.
2. **Tabular Enrichment**: Joins non-spatial snowfall prediction data to the road network using `DatabaseJoiner`.
3. **Styling with KML**: Applies styling rules to features for Google Earth-compatible output using `KMLStyler`.
4. **Attribute Cleanup**: Modifies text attributes using `StringReplacer` for standardization.
5. **FME Flow Upload**: Publishes the final product to an FME Flow resource using `FMEFlowResourceConnector`.

---

## Key Takeaway  
This exercise shows how to automate a real-world ETL pipeline involving archive extraction, attribute enrichment, styling for KML delivery, and web-based publishing. It demonstrates seamless integration between desktop FME workflows and server-side deployment using FME Flow—critical for scalable, automated data pipelines.

---

*Below is a screenshot of the final workspace used in this module:*

![Workspace screenshot](https://github.com/user-attachments/assets/7746f160-316c-4c9e-8229-2c1d6065cc3a)

---

> This project reflects advanced handling of multi-source data (archives + web), styling logic, and cloud publishing—all in a single automated FME workflow.
