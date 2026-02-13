# Advanced Reading & Writing

## Skills Gained

- Reading multiple feature types from a **GML (Geography Markup Language)** dataset
- Writing outputs to **multiple Excel sheets** and **GML files** using **Feature Type Fanout**
- Organizing the workspace with **multiple writers** and controlling the **writer order**
- Renaming feature types and customizing output using **Writer Parameters**
- Automating schema definitions and attribute mapping
- Using the **Inspector** for output validation

---

## Workflow

### Input:
- A single GML dataset containing several layers (e.g., Parcels, Roads, Zoning)

### Process:
- Fanout by Feature Type to organize outputs
- Rename feature types and apply writer settings per format
- Use Excel and GML writers simultaneously
- Set writer order to ensure dependencies (e.g., Zoning written last)

### Output:
- One Excel workbook with multiple sheets (Parcels, Roads, Zoning)
- Separate GML files split by feature type

---

## Key Learnings

| Concept | What I Learned |
|--------|----------------|
| Feature Type Fanout | Automatically direct features into separate outputs based on type |
| Multiple Writers | Add and manage more than one output format in the same workspace |
| Writer Order | Control the execution order of outputs (important for dependencies) |
| Writer Parameters | Rename output sheets/files dynamically and structure them meaningfully |
| Schema Mapping | Handle mismatches and automate output schema setup |
| Workspace Organization | Maintain readability and performance for complex outputs |

---

## Outcome

- Gained confidence in handling **multi-format outputs** in FME
- Understood how to **structure real-world ETL workflows** using multiple writers
- Improved skills in schema automation and writer configuration
- Reinforced best practices for workspace clarity and scalability

---

## Files in This Repo
```
Advanced_Reading_Writing/
├── Advanced_Reading_Writing.md # Notes and instructions for advanced workspace design
├── CommunityMap.gdb.zip # Zipped Geodatabase with community mapping data
├── Design Workspaces for Advanced Reading and Writing.PNG # Visual guide or reference image
└── exercise-set-reader-and-writer-parameters-complete.fmw # Final FME workspace with configured parameters
```
