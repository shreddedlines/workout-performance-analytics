# Workout Performance Analytics  (End-to-End Analytics Project)
 (Python, SQL Server, Power BI)

This project is an end-to-end data analytics pipeline built using real-world, unstructured personal workout data. Raw workout logs recorded in WhatsApp were extracted, combined with historical training data, transformed into structured datasets, analyzed using SQL, and finally presented through a KPI-driven Power BI dashboard.

The Power BI dashboard represents the final presentation layer. The core of the project lies in data extraction, data integration, feature engineering, analytical querying, and metric interpretation.

---

## Project Objective

The objective of this project is to build a complete analytics system to answer the following questions:

- How has strength progressed over time?
- How does strength behave relative to bodyweight?
- How do performance patterns differ between bulk and cut phases?
- How is training volume distributed across muscle groups?
- Are there indications of potential recovery-related stress?

The focus is on descriptive and diagnostic analytics rather than prediction or machine learning.

---

## Data Sources

### WhatsApp Workout Logs (Unstructured)
- Primary source of recent training data
- Text-based and unstructured workout logs
- Inconsistent exercise naming, formats, and units
- Recorded across different gyms and training phases

### Previous Training Records (Structured)
- Older historical training data recorded separately
- Used to maintain continuity across training periods

For privacy reasons, raw WhatsApp chat exports are not included. Only cleaned and analytical datasets are shared.

---

## Data Integration

After extracting workout data from WhatsApp logs, the extracted dataset was combined with previously recorded historical training data. This ensured:

- Continuity across training periods
- Preservation of older workout records
- A single unified dataset for downstream analysis

The merged dataset served as the base for all subsequent feature engineering and analysis.

---

## Data Cleaning and Feature Engineering (Python)

Using Python (Pandas and NumPy), the following steps were performed:

- Parsed unstructured WhatsApp logs into structured tabular data
- Standardized exercise names and resolved inconsistencies
- Mapped exercises to muscle groups
- Normalized weight units across different gyms
- Calculated training volume (weight × reps)
- Estimated strength using the Epley 1RM formula
- Computed relative strength (strength adjusted for bodyweight)
- Aggregated exercise-level data into weekly performance metrics
- Labeled training phases (Bulk and Cut)
- Derived recovery-related indicators based on strength trends

Final analytical datasets:
- feature_engineered_data.csv — exercise and set-level engineered data  
- workout_weekly_analysis.csv — weekly aggregated performance metrics  

---

## Analytical Querying (SQL Server)

The weekly analytical dataset was loaded into SQL Server for structured querying.

SQL analysis was organized into multiple focused scripts, each answering a specific analytical question:

- Average relative strength by phase and muscle group
- Strength comparison by gym type
- Strength distribution across muscle groups
- Identification of under-recovered weeks
- Weekly total training volume analysis

Sample SQL execution screenshots are included to demonstrate query execution and results.

---

## Visualization and Decision Layer (Power BI)

A KPI-driven Power BI dashboard was built as the final decision and presentation layer.

Dashboard features include:

- Executive KPIs for estimated strength (E1RM), relative strength, and bodyweight
- Dynamic metric selection (Average, Maximum, Robust Minimum using percentiles)
- Monthly strength and relative strength trend analysis
- Bodyweight versus relative strength comparison
- Training volume distribution by muscle group
- Bulk versus cut phase comparison
- Recovery status overview

The dashboard enables multi-perspective performance evaluation while avoiding misleading conclusions from simple averages.

---

## Key Insights

- Relative strength remained more stable than absolute strength during cutting phases.
- Bodyweight trends provide essential context for interpreting strength changes.
- Training volume distribution highlights muscle group emphasis and imbalance.
- Percentile-based minimum metrics prevent outlier weeks from distorting conclusions.

---

## Tools and Technologies

- Python — Pandas, NumPy (data extraction, cleaning, and feature engineering)
- SQL Server — analytical querying and aggregation
- Power BI — data modeling, DAX measures, KPI-driven dashboards
- GitHub — version control and project presentation

---

---

## What This Project Demonstrates

- Handling messy, unstructured real-world data
- Data integration from multiple sources
- Strong feature engineering and aggregation logic
- Practical SQL-based analytical thinking
- KPI-first dashboard design
- Ability to build an end-to-end analytics workflow, not just visualizations

---

## Note

This project intentionally avoids machine learning to maintain interpretability and analytical rigor, focusing instead on clear, decision-ready insights.

## Author
**Kshitish**  
Data Science Undergraduate  
Interested in data analysis, performance tracking, and building insight-driven systems
