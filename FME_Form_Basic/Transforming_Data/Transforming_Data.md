# FME Form: Transforming Data Exercise

## Overview

This covers how to read JSON data from an API, extract and transform spatial and non-spatial data, join it with local datasets, and output a cleaned and sorted result.

---

## Tools Used

- FME Workbench
- FME Data Inspector

---

## Project Workflow:

1. **Fetch JSON Data** using `HTTPCaller` from a web URL.
2. **Parse JSON** with `JSONFragmenter` to extract individual records.
3. **Create Geometries** using coordinates with `VertexCreator`.
4. **Set Coordinate System** to ensure proper spatial referencing.
5. **Manage Attributes** to clean and prepare data for joining.
6. **Join Web Data with Local Data** using `DatabaseJoiner`.
7. **Remove Unwanted Attributes** using `AttributeRemover`.
8. **Sort Features Alphabetically** by `last_name` using `Sorter`.
9. **Filter Final Output** using `Tester` before writing the final data to output.

---

## Transformers Applied

| Transformer            | Purpose                                                                 |
|------------------------|-------------------------------------------------------------------------|
| `Creator`              | Starts the workflow                                                     |
| `HTTPCaller`           | Fetches live data from a web API                                        |
| `JSONFragmenter`       | Parses JSON and extracts data records                                   |
| `VertexCreator`        | Converts coordinate values into spatial geometries                      |
| `CoordinateSystemSetter` | Assigns a spatial reference system                                     |
| `AttributeManager`     | Renames, reorders, or removes unnecessary attributes                     |
| `DatabaseJoiner`       | Joins web data with an external dataset                                 |
| `AttributeRemover`     | Removes attributes like `_matched_records` before output                |
| `Sorter`               | Sorts data alphabetically based on the `last_name` attribute            |
| `Tester`               | Filters valid records before writing to output                          |

---

## Learnings

- Gained experience working with web APIs inside FME  
- Learned how to join external and internal datasets using key fields  
- Understood the importance of attribute management in clean data delivery  
- Practiced layout organization, annotation, and efficient workspace execution  
- Completed the project with real-time execution captured on video, validating my practical FME skills

---

# FME Form - Join Tables

## Objective

To learn how to join data tables using the Joiner transformer

## Skills Gained:

- Joining spatial and non-spatial datasets

- Understanding key fields for data relationships

- Filtering and matching join attributes

- Using the FME Data Inspector to verify results

---

## Learnings
- To use the Joiner transformer to enrich spatial data with attribute information

- Importance of matching key fields when joining datasets

- To visually inspect join results using the Data Inspector
