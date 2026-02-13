# Code Review a Colleague’s Workspace – FME Form Advanced

## Project Overview

This mini-project focuses on performing a **best-practice code review** of an FME workspace created by another user. The task involves identifying inefficiencies, cleaning up unnecessary elements, standardizing attribute handling, and ensuring the workspace meets spatial data transformation standards. The goal is to practice critical assessment and refactoring of FME workflows—a vital skill for production-ready data pipelines.

---

## Core Tools Used

* **AttributeCreator / AttributeRemover** – For attribute cleanup and consolidation
* **Multiple Readers & Writers (FileGDB, Shapefile, etc.)** – Handle diverse input sources and formats
* **Annotations** – For documenting observations and required changes
* **Best Practices** – Applying coordinate system alignment, schema cleanup, and transformer reusability

---

## Inputs & Outputs

| Input Dataset                                       | Output Format                                                                |
| --------------------------------------------------- | ---------------------------------------------------------------------------- |
| Mixed civic data (Libraries, Parks, Garbages, etc.) | Cleaned datasets categorized by theme (e.g., Community, Environment, Safety) |

Example:

* Input: Unorganized multi-layer civic data
* Output: Clean, thematically grouped layers (Community, Environment, Food, Transit, Safety)

---

## Workflow Highlights

1. **Coordinate System Standardization**: Adjust projection settings for all spatial inputs to ensure alignment.
2. **Attribute Cleanup**: Use AttributeRemover and AttributeCreator to keep only relevant attributes.
3. **Thematic Grouping**: Categorize features into meaningful outputs—Community, Safety, Environment, etc.
4. **Metadata Enhancement**: Add/standardize fields like `Editor`, `Source`, or `UpdateDate` where missing.
5. **Efficiency Refactor**: Remove duplicate or unnecessary transformers, comments, and encoding issues.

---

## Key Takeaway

This project highlights the importance of **maintainable, readable, and optimized FME workflows**. Performing code reviews fosters collaboration, quality control, and prepares analysts for team environments or enterprise-scale deployment where consistency and clarity matter.

---

*Workspace Screenshot*:

![Workspace Screenshot](https://github.com/user-attachments/assets/069880f7-fd97-40ff-acab-3bacb640cc26)

---

> This project showcases your ability to evaluate and enhance existing FME workflows through structured code review.
