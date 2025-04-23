# Sales Analysis and Customer Segmentation Project

This project automates a complete customer segmentation workflow, integrating raw input from Google Sheets, clustering analysis with K-Prototypes, and daily-updated Power BI dashboards. It's designed to provide marketing and sales teams with actionable insights — fully automated, cloud-based, and production-ready.

---

## Project Summary

This pipeline ingests raw datasets from Google Sheets, applies customer segmentation using the **K-Prototypes algorithm**, and loads results into **Google BigQuery**, where **Power BI dashboards** provides business insights about the sales and customer segments. The entire process is automated using **GitHub Actions** and scheduled to run daily at 10pm London time**.

---
## Technologies Used

- **Python**: `pandas`, `kmodes`, `gower`, `prince`, `sklearn`, `pandas-gbq`
- **GitHub Actions**: automation of Python scripts
- **Google BigQuery**: SQL
- **Power BI**: real-time dashboards

---
## Highlights

- Fully automated from raw data to dashboard insights
- Real-world use of **mixed-type clustering** with K-Prototypes
- CI/CD-ready pipeline with GitHub Actions
- Cloud-native design using BigQuery + Power BI
- Business-friendly, scalable, and no manual refreshes required

---
## ETL Process
!(./ETL_pipeline.png)
---

## Workflow Overview

1. **Data Collection**  
   - Raw tables (`customers`, `sales`, `products`) maintained in Google Sheets by business users (e.g. Sales Department)

2. **Data Processing + Clustering**  
   - Python script at **Google Colab** loads data, cleans it, and applies **K-Prototypes clustering**
   - Mixed-type features handled using **FAMD** and **Gower distance**
  
3. **GitHub Actions Automation**  
   - Python script is loaded to Github and is scheduled to run daily using GitHub Actions
   - Uses **secure service account authentication** via GitHub Secrets

4. **BigQuery Integration**  
   - Processed datasets are written to **Google BigQuery**
   - Clean **SQL views** are created for use in reporting

5. **Power BI Dashboard**  
   - Power BI connects directly to BigQuery views
   - Dashboards auto-refresh daily at 11pm London time to reflect the most current segmentation and sales data

---

## Schedule & Maintenance

| Layer           | Schedule             | Managed By         |
|----------------|----------------------|---------------------|
| Python Script  | Daily @ 10 PM BST    | GitHub Actions      |
| BigQuery Views | Live / real-time     |                     |
| Power BI       | Daily @ 11 PM BST    | Power BI Scheduler  |

---
