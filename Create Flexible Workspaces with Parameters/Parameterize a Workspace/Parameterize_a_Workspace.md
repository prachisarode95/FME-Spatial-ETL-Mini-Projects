# Parameterize a Workspace – FME Form Advanced

## Project Overview

This mini-project demonstrates how to design a flexible and user-responsive workspace in FME using **published parameters**. The workflow reads park data and enables user-defined metadata (e.g., Author Name, Date) to be embedded dynamically into both spatial and tabular outputs. It showcases **customization and reusability**, key for scalable geospatial ETL pipelines.

---

## Core Tools Used

* **MITAB Reader/Writer** – For reading and writing park spatial data
* **Sampler** – To extract a sample feature for metadata creation
* **AttributeCreator** – Adds static and parameterized values
* **ParameterFetcher** – Pulls user-specified values from published parameters
* **Published Parameters** – For custom author info, notes, and update date

---

## Inputs & Outputs

| Input Dataset       | Output Format                       |
| ------------------- | ----------------------------------- |
| `Parks.tab` (MITAB) | Updated `Parks.tab` with metadata   |
| `ParksMetadata.tab` | Tabular MITAB with metadata summary |

Example:

* Input: Vector layer of park features
* Output:

  1. A spatial dataset with added custom attributes
  2. A metadata summary layer for review and QA

---

## Workflow Highlights

1. **Load Parks Data** using MITAB reader.
2. **Select Sample Feature** using the Sampler transformer for metadata extraction.
3. **Add Metadata Fields** such as `AuthorEmail`, `Notes`, and `UpdateDate` using AttributeCreator.
4. **Fetch User Inputs** via ParameterFetcher tied to published parameters.
5. **Write Outputs** to dynamically named .tab files using embedded user information.

---

## Key Takeaway

This project highlights the importance of **parameterization in ETL workflows**. By making workspaces adaptable to user input, it supports reusability, reduces hardcoding, and aligns with best practices in enterprise GIS automation. It's especially valuable in workflows that demand stakeholder-specific metadata injection.

---

*Workspace Screenshot*:

![Workspace Screenshot](![Image](https://github.com/user-attachments/assets/a78c27b5-eeae-4447-85cd-caccb924cb26)

---

> This project showcases advanced FME workspace flexibility using published parameters, making it easier to scale and customize spatial data processing.
