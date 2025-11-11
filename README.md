
# 🌞 Solar Data Discovery – Week 0 Challenge

**Author:** Kalkidan Asdesach
**Branch:** main
**Date:** November 2025

---

## **Project Overview**

This project is part of the **Solar Data Discovery Challenge – Week 0**, aimed at analyzing solar energy potential across **Benin, Togo, and Sierra Leone**.

The goal is to **explore, clean, visualize, and compare solar datasets** to identify patterns, assess solar irradiance, and provide actionable insights for energy planning.

---

## **Datasets**

The following datasets were used (all included in `data/`):

| Country      | File Name                 | Description                                                         |
| ------------ | ------------------------- | ------------------------------------------------------------------- |
| Benin        | `benin-malanville.csv`    | Solar irradiance, temperature, humidity, module readings, wind data |
| Togo         | `togo-dapaong_qc.csv`     | Same metrics as Benin                                               |
| Sierra Leone | `sierraleone-bumbuna.csv` | Same metrics as Benin                                               |

**Key Columns:**

* `GHI` – Global Horizontal Irradiance (W/m²)
* `DNI` – Direct Normal Irradiance (W/m²)
* `DHI` – Diffuse Horizontal Irradiance (W/m²)
* `Tamb` – Ambient temperature (°C)
* `RH` – Relative humidity (%)
* `ModA / ModB` – Solar module readings
* `WS / WSgust / WD` – Wind speed, gust, and direction

---

## **Project Structure**

```
solar-challenge-week0/
├── .github/workflows/
   # CI workflows
│
├─ data/                      
│  ├─ benin-malanville.csv
│  ├─ togo-dapaong_qc.csv
│  ├─ sierraleone-bumbuna.csv
│
├─ src/
│  └─ notebooks/
│      ├─ benin_eda.ipynb
│      ├─ togo_eda.ipynb
│      ├─ sierraleone_eda.ipynb
│      └─ compare_countries.ipynb
    ├── scripts/        
│   └── __init__.py
    ├── tests/        
│   └── __init__.py

├── .gitignore
├── README.md
└── requirements.txt
```

---

## **Workflow**

### **1️⃣ Per-Country EDA**

* Load datasets and inspect missing values.
* Detect and impute **outliers** using Z-scores and median imputation.
* Perform **time-series analysis** of irradiance and temperature.
* Visualize **correlations**, wind, and module performance.
* Generate **summary statistics**.

### **2️⃣ Cross-Country Comparison**

* Compare **GHI, DNI, DHI** distributions using boxplots.
* Compute descriptive statistics: mean, median, standard deviation.
* Perform **ANOVA/Kruskal-Wallis** tests to check for significant differences.
* Rank countries by average GHI for visual summary.

---

## **Key Findings**

* **Benin:** Highest median GHI → strong solar potential.
* **Togo:** Lower DNI → fewer direct sunlight hours.
* **Sierra Leone:** Most consistent DHI → high diffuse irradiance under clouds.
* Correlations show **strong relationships** between irradiance metrics and temperature/humidity.
* Statistical tests confirm **significant differences in solar potential** across countries.

---

## **Tools & Libraries**

* **Python 3.x** – pandas, numpy, matplotlib, seaborn, scipy, windrose
* **Jupyter Notebook** – analysis and visualizations
* **Git & GitHub** – version control
* **VS Code** – coding and notebook editing

---

## **How to Run**

1. Clone the repository:

```bash
git clone https://github.com/<your-username>/solar-challenge-week0.git
cd solar-challenge-week0
```

2. Create a virtual environment and install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate      # Mac/Linux
.venv\Scripts\activate         # Windows
pip install -r requirements.txt
```

3. Open Jupyter Notebook:

```bash
jupyter notebook
```

4. Explore notebooks in `src/notebooks/`:

   * `benin_eda.ipynb`
   * `togo_eda.ipynb`
   * `sierraleone_eda.ipynb`
   * `compare_countries.ipynb`

---

## **Results & Visualizations**

* Boxplots of GHI, DNI, DHI per country
* Average GHI ranking bar chart
* Time-series plots of irradiance and temperature
* Correlation heatmaps
* Module performance pre/post cleaning

---

## **Conclusion**

This Week 0 analysis provides a **comprehensive view of solar potential** across three West African countries:

* **High-quality cleaned datasets** ensure reliable insights.
* **Cross-country comparisons** highlight regional differences.
* Statistical testing and visualizations make results **actionable for energy planning**.

Future work will involve **predictive modeling** and more advanced solar performance analysis in Week 1.

---

## **License**

MIT License – feel free to use this project for **educational purposes**.

 
