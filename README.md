# Healthcare Operations Impact Analytics
Includes structured KPI engineering, operational benchmarking, and executive-level performance insights.

---

## Executive Summary

This project builds a scalable analytics framework to evaluate healthcare operational performance using structured KPI engineering and visualization.

By transforming raw hospital encounter data into decision-ready metrics, the analysis identifies patterns in clinical complexity, efficiency, and operational variability across sites and specialties.

The framework enables healthcare leaders to detect performance differences, monitor trends, and optimize resource allocation using data-driven insights.

---

## Business Problem

Healthcare systems operate under constrained resources while managing fluctuating patient demand and case complexity.

Operational leaders need standardized metrics to answer questions such as:

- Which sites manage more complex cases?
- Where are operational inefficiencies occurring?
- How does performance vary over time?
- Which locations deliver higher output relative to effort?

Without structured analytics, these insights remain hidden inside raw data.

---

## Project Overview

This project develops a structured analytics framework to evaluate operational performance in a healthcare setting.  
The goal is to transform raw hospital operational data into meaningful Key Performance Indicators (KPIs) that support data-driven decision making.

The analysis focuses on:

- Measuring operational efficiency  
- Quantifying impact per encounter  
- Comparing performance across insurance payers and medical specialties  
- Creating reusable datasets for reporting and strategic planning  

---

## Business Objective

Healthcare organizations need clear metrics to understand how resources and clinical complexity vary across different payers and specialties.

This project answers questions such as:

- Which insurance payers generate higher clinical complexity per encounter?
- How does impact vary month to month?
- Which medical specialties show higher operational load?
- How many unique patients and encounters occur each month?

---

## Dataset Description

The project uses a hospital operations dataset containing the following key fields:

- **Month** – encounter month  
- **Case_No** – unique patient/encounter identifier  
- **Specialty** – medical department or service line  
- **Insurance/Payer** – financial payer category  
- **Doctor Status** – operational outcome/status  
- **CMI Value** – Case Mix Index (used as impact proxy)

> **Note:**  
> The dataset does not contain real financial cost fields.  
> Therefore, the analysis uses **CMI Value (Case Mix Index)** as a proxy metric for clinical impact and operational complexity.

---

## Key Insights

Analysis revealed several operational patterns:

- Clear variability in complexity across sites and payers
- Seasonal fluctuations in impact per encounter
- Differences in outcome resolution rates between locations
- Detectable efficiency differences when comparing volume vs impact

These insights suggest that operational performance is not uniform and can be optimized through targeted interventions.

---

## Strategic Recommendations

Based on the analysis, healthcare administrators could:

- Investigate high-impact sites to identify complexity drivers
- Replicate workflows from efficient locations
- Adjust staffing models during peak complexity periods
- Optimize payer mix strategy based on operational load
- Monitor outcome metrics as quality indicators

---
## Business Impact

Implementing this analytics framework could support:

- More efficient resource allocation
- Reduced operational cost variability
- Improved service delivery consistency
- Faster executive decision-making
- Stronger performance monitoring infrastructure

The project demonstrates how structured analytics transforms raw data into actionable operational intelligence.

---

## Analytical Approach

The project follows a structured analytics pipeline:

1. **Data Ingestion**
   - Automatic detection and loading of CSV files  
   - Standardization of column names  

2. **Data Cleaning & Transformation**
   - Date parsing and normalization  
   - Creation of analytical dimensions  
   - Construction of outcome flags  
   - Aggregation to monthly level  

3. **Metrics Engineering**
   - Development of reusable KPI framework  
   - Aggregation by month, payer, and specialty  

4. **Visualization & Reporting**
   - Trend analysis of impact per encounter  
   - Exportable datasets for BI tools  

---

## Key Performance Indicators (KPIs)

The following KPIs are calculated:

| KPI | Description |
|----|------------|
| Encounters | Unique medical cases per period |
| Patients | Unique patients per period |
| Total Impact Proxy | Sum of CMI values |
| Impact per Encounter | Average impact per case |
| Impact per Patient | Average impact per patient |
| Resolved Rate | Percentage of resolved cases |
| Referred Rate | Percentage of referred cases |

---

## Executive Visual Insights

To complement the KPI framework, the project includes a structured visual analytics layer designed to support executive decision-making.

1️⃣ Monthly Impact Trend

![Trend](outputs/figures/01_trend_cost_per_encounter.png)

Reveals time-based variation in operational complexity, highlighting potential seasonal resource intensity.

---

2️⃣ Site-Level Benchmarking

![Ranking](outputs/figures/02_site_ranking_cost_per_encounter.png)

Shows structural differences in impact per encounter across payers/sites, enabling comparative performance analysis.

---

3️⃣ Operational Heatmap (Site × Month)

![Heatmap](outputs/figures/03_heatmap_site_month_cost_per_encounter.png)

Identifies temporal spikes and recurring patterns in complexity across sites.

---

4️⃣ Outcome Performance

![Outcomes](outputs/figures/04_outcomes_by_site.png)

Compares resolved and referred rates, highlighting differences in operational workflow and case handling.

---

5️⃣ Efficiency Landscape (Volume vs Impact)

![Efficiency](outputs/figures/05_efficiency_volume_vs_cost.png)

Maps total encounter volume against impact per encounter to identify relative operational efficiency.

---

## Sample Output

The project produces:

- Monthly KPIs by **Insurance/Payer**
- Monthly KPIs by **Medical Specialty**
- Trend visualizations of impact per encounter

Example insight generated:

> "BlueMedic Charity shows higher average impact per encounter in mid-2025 compared to commercial insurers, suggesting higher case complexity among charity-supported patients."

---

## Project Structure

```
healthcare-operations-impact/
│
├── data/
│   ├── raw/            # Original dataset from Kaggle
│   └── processed/      # Cleaned and aggregated KPI tables
│
├── notebooks/
│   └── 01_build_kpis.ipynb   # Full analytics pipeline
│
├── reports/            # Saved charts and outputs
├── src/                # Reusable scripts (optional)
└── README.md
├── outputs/
│   └── figures/       # Generated visualization outputs
```

---

## How to Run the Project

1. Clone the repository

```
git clone https://github.com/denpareja/healthcare-operations-impact.git
cd healthcare-operations-impact
```

2. Install dependencies

```
pip install pandas numpy matplotlib
```

3. Place the dataset CSV file inside:

```
data/raw/
```

4. Open and run the notebook:

```
notebooks/01_build_kpis.ipynb
```

5. Processed outputs will be generated in:

```
data/processed/
```

---

## Generated Files

The notebook exports the following structured datasets:

- **kpis_month_site.csv** – KPIs aggregated by payer  
- **kpis_month_program.csv** – KPIs aggregated by specialty  
- **kpi_catalog.csv** – Documentation of metric definitions  

These files can be directly connected to Power BI, Tableau, or Excel for further analysis.

---
## Executive Summary

This project builds a reusable healthcare operational benchmarking framework.

Key findings include:

- Detectable variability in case complexity across sites and specialties  
- Temporal fluctuations in impact per encounter  
- Differences in resolution and referral performance  
- Clear efficiency differentiation based on volume and complexity  

The framework enables data-driven decisions in:

- Resource allocation  
- Capacity planning  
- Performance monitoring  
- Strategic payer mix evaluation  
---

## Limitations

- The dataset does not include real financial costs.  
- CMI Value is used as a **proxy for impact**, not as a true monetary measure.  
- Time spent per encounter is not available.

---

## Future Improvements

Potential extensions of this project:

- Incorporate real billing or cost data  
- Add provider-level productivity metrics  
- Predict high-impact specialties using machine learning  
- Build an interactive dashboard  

---

## Tools Used

- Python  
- pandas  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

---

## Executive Takeaway

Operational performance differences are measurable, explainable, and optimizable when healthcare data is structured into meaningful KPIs.

Data alone does not drive decisions. Structured analytics does.

---

## Consulting Relevance

This project mirrors real-world healthcare analytics consulting engagements where organizations require:

- Operational benchmarking
- KPI framework design
- Efficiency diagnostics
- Performance monitoring systems

It demonstrates the ability to translate raw datasets into executive-level insights and strategic recommendations.

---

## Skills Demonstrated

- Healthcare operations analytics  
- KPI engineering  
- Case Mix Index proxy modeling  
- Time-series trend analysis  
- Performance benchmarking  
- Operational efficiency mapping  
- Executive-level data storytelling  
- Reproducible analytics pipeline design

---

## Author

**Denisse Pareja**  
Healthcare Analytics Consultant | Data Scientist

Specialized in building decision-driven analytics systems that translate data into strategic insight for healthcare and operational organizations.

LinkedIn: https://linkedin.com/in/TUURL
GitHub: https://github.com/denpareja

---

## Portfolio Note
This project is part of a professional analytics portfolio focused on developing decision-intelligence frameworks that help organizations move from descriptive reporting to predictive and strategic analytics.
