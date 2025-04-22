# Customer Segmentation Pipeline (Automated with GitHub Actions + BigQuery + Power BI)

This project automates a complete customer segmentation workflow, integrating raw input from Google Sheets, clustering analysis with K-Prototypes, and daily-updated Power BI dashboards. It's designed to provide marketing and sales teams with actionable insights — fully automated, cloud-based, and production-ready.

---

## Project Summary

This pipeline ingests raw datasets from Google Sheets, applies customer segmentation using the **K-Prototypes algorithm**, and loads results into **Google BigQuery**, where **Power BI dashboards** visualize the final segments. The entire process is automated using **GitHub Actions** and scheduled to run daily at **8:20 AM London time**.

---

## Workflow Overview

1. **Data Collection**  
   - Raw tables (`customers`, `sales`, `products`) maintained in Google Sheets by business users

2. **Data Processing + Clustering**  
   - Python script loads data, cleans it, and applies **K-Prototypes clustering**
   - Mixed-type features handled using **FAMD** and **Gower distance**

3. **BigQuery Integration**  
   - Processed datasets are written to **Google BigQuery**
   - Clean SQL **views** are created for use in reporting

4. **Power BI Dashboard**  
   - Power BI connects directly to BigQuery views
   - Dashboards auto-refresh daily to reflect the most current segmentation

5. **GitHub Actions Automation**  
   - Python script is scheduled to run daily using GitHub Actions
   - Uses **secure service account authentication** via GitHub Secrets
   - Cron-based schedule: **7:20 AM UTC = 8:20 AM London time**

---

## Technologies Used

- **Python**, `pandas`, `kmodes`, `gower`, `prince`, `sklearn`
- **Google Sheets API**
- **Google BigQuery** + `pandas-gbq`
- **GitHub Actions** for automation and CI/CD
- **Power BI** for real-time dashboards

---

## Highlights

- Fully automated from raw data to dashboard insights
- Real-world use of **mixed-type clustering** with K-Prototypes
- CI/CD-ready pipeline with GitHub Actions
- Cloud-native design using BigQuery + Power BI
- Business-friendly, scalable, and no manual refreshes required

---

## Optional: Screenshots / Demo

_Add screenshots of your Power BI dashboard here!_

---

## Schedule & Maintenance

| Layer           | Schedule             | Managed By          |
|----------------|----------------------|---------------------|
| Python Script  | Daily @ 8:20 AM BST  | GitHub Actions      |
| BigQuery Views | Live / real-time     | No scheduling needed|
| Power BI       | Daily (after Python) | Power BI Scheduler  |

---
