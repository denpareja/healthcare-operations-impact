# Healthcare Operations Impact Analytics

**TripleTen Bootcamp – Data Science Project | 2025**

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

## Technologies Used

- Python  
- pandas  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

---

## Author

**Denisse Pareja**  
Data Scientist – TripleTen Bootcamp  
2025  
