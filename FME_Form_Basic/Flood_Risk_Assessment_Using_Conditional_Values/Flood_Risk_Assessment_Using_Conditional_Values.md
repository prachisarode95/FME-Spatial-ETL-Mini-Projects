# Flood Risk Assessment Using Conditional Values Using FME Form Tools

## About the exercise

This is a hands-on exercise from the **FME Form Basic course** by Safe Software. It demonstrates **how to assign flood risk scores to address points by using conditional logic based on elevation and proximity to coastal zones.** The entire workflow was built and executed using **FME Workbench 2024.2**, showcasing **real-world attribute transformation** and **spatial analysis techniques.**

---

## Tools Used

- **FME Workbench**  
  For designing, building, and executing the flood risk assessment workflow.

- **FME Data Inspector**  
  To visually inspect and verify the flood risk values assigned to each address.

---

## Workflow Overview

1. **Read Input Datasets**:  
   - Postal addresses  
   - Coastal zones  
   - Digital elevation model (DEM)

2. **Identify Addresses Near the Coast**:  
   - Use `PointOnAreaOverlayer` to overlay addresses with coastal zone boundaries.
   - Apply `Tester` to select addresses within specified distances (100m, 200m, 300m).

3. **Extract Elevation Values**:  
   - Use `Reprojector` to match the DEM and address projections.
   - Apply `PointOnRasterValueExtractor` to extract elevation values from the DEM.

4. **Clean Attribute Names**:  
   - Use `AttributeRenamer` to tidy up and standardize attribute names.

5. **Assign Flood Risk Score**:  
   - Use `AttributeManager` with conditional values to assign a risk score based on elevation and proximity.

6. **Write Final Output**:  
   - Export the enriched dataset with flood risk scores assigned to each address.

---

## Transformers Applied

| Transformer                  | Purpose                                                                |
|-------------------------------|------------------------------------------------------------------------|
| `PointOnAreaOverlayer`        | Determines spatial relationship between addresses and coastal zones   |
| `Tester`                     | Filters addresses within coastal proximity thresholds                |
| `Reprojector`                 | Aligns coordinate systems for raster and vector data                 |
| `PointOnRasterValueExtractor` | Extracts elevation values for address points from DEM                |
| `AttributeRenamer`            | Cleans and simplifies attribute names                                |
| `AttributeManager`            | Assigns conditional flood risk scores based on elevation and location |

---

## Key Output

- A postal address dataset enriched with a new `FloodRiskScore` attribute.
- Scores are dynamically assigned based on distance to coast and elevation values.
- Clean, ready-to-use output for flood risk analysis and decision-making.

---

## Learnings & Reflection

✔️ Gained hands-on experience combining raster and vector data  
✔️ Practiced using conditional expressions within `AttributeManager`  
✔️ Improved skills in overlay analysis and attribute management  
✔️ Understood the importance of data preparation for spatial risk analysis  
✔️ Completed a mini-project demonstrating both spatial and attribute transformations in FME

---

## File Structure
```
Flood_Risk_Assessment_Using_Conditional_Values/
├── exercise-flood-risk-project-complete.fmw # Final FME workspace using conditional logic
├── Flood_Risk_Assessment_Using_Conditional_Values.md # Project documentation and explanation
└── flood_risk_project_demo.mp4 # Demo video walkthrough of the flood risk workflow
```
---
