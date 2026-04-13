# 📊 UCSD STEM Course Insights

> **What makes students recommend a course?** This project analyzes 61,000+ UCSD student evaluations to uncover what drives course satisfaction — from instructor quality to class size.

---

## 🔍 Research Question

**How do factors such as course workload, instructor quality, grade expectations, and enrollment size correlate with student satisfaction in UCSD STEM courses (2020–2022)?**

---

## 📦 Dataset

- **Source:** [UCSD Historical Enrollment Data — CAPEs.tsv](https://github.com/UCSD-Historical-Enrollment-Data/UCSDHistEnrollData/blob/master/data/CAPEs.tsv)
- **Scope:** 61,791 course-section observations across 14 UCSD STEM departments (2020–2022)
- **Key Variables:** instructor & class recommendation rates, weekly study hours, expected vs. received GPA, enrollment size

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-lightblue?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Analysis-blue?logo=numpy)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Statsmodels](https://img.shields.io/badge/Statsmodels-OLS%20Regression-green)
![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Tests-blueviolet)

---

## 📈 Key Findings

- **Instructor quality** is the #1 driver — Pearson correlation of **0.79** between instructor and class recommendation rates, consistent across all departments
- **Higher workload** slightly lowers satisfaction — each additional study hour/week corresponds to a **~1.3% drop** in recommendation rate (R² = 0.051)
- **Grade expectations** matter — students whose grades met or exceeded expectations recommended at **87.16% vs. 83.39%**
- **Smaller classes** (20–94 students) score slightly higher than large ones (95–1,101), though class size alone explains only **0.5% of variance**

---

## 💡 Conclusions

Instructor quality dominates student course satisfaction across all STEM departments. Workload, grade expectations, and class size all have measurable but secondary effects. Findings offer practical guidance for students choosing courses and institutions improving teaching effectiveness.

---

## 📌 Acknowledgements

- Data provided by [UCSD Historical Enrollment Data](https://github.com/UCSD-Historical-Enrollment-Data)
- Project completed as part of **COGS 108: Data Science in Practice** at UC San Diego (Winter 2025)
