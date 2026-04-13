# 📊 UCSD STEM Course Insights

> **What makes students recommend a course?** This project analyzes 61,000+ UCSD student evaluations to uncover what drives course satisfaction — from instructor quality to class size.

---

## 🔍 Research Question

**How do factors such as course workload, instructor quality, grade expectations, and enrollment size correlate with student satisfaction in UCSD STEM courses (2020–2022)?**

---

## 📦 Dataset

- **Source:** [UCSD Historical Enrollment Data — CAPEs.tsv](https://github.com/UCSD-Historical-Enrollment-Data/UCSDHistEnrollData/blob/master/data/CAPEs.tsv)
- **Scope:** UCSD STEM courses from 2020–2022 academic years
- **Size:** 61,791 course-section observations across 14 STEM departments
- **Key Variables:**
  - `rcmd_class` — % of students who recommend the course
  - `rcmd_instr` — % of students who recommend the instructor
  - `study_hr_wk` — Average weekly study hours reported
  - `avg_grade_exp` / `avg_grade_rec` — Expected vs. received GPA
  - `enroll` — Course enrollment size

> ⚠️ The raw data file is not included in this repo due to size. Download it from the link above and place it in the `data/` folder as `CAPEs.tsv`.

---

## 📁 Project Structure

```
UCSD-Course-Insights/
├── data/                    # Data folder (see Dataset section above)
├── FinalProject.ipynb       # Full analysis and findings
├── EDA_Checkpoint.ipynb     # Exploratory data analysis checkpoint
├── Data_Checkpoint.ipynb    # Data wrangling checkpoint
├── Project_Proposal.ipynb   # Original project proposal
└── README.md
```

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

### 1. 👩‍🏫 Instructor Quality is the #1 Driver
- **Pearson correlation of 0.79** between instructor recommendation and class recommendation
- Consistent across all 14 STEM departments (Spearman ρ ranging from 0.575–0.841)
- Instructor perception is by far the strongest predictor of whether students recommend a course

### 2. 📚 Higher Workload = Lower Satisfaction
- OLS regression found a **weak but statistically significant negative relationship** (R² = 0.051)
- Each additional study hour per week is associated with a **~1.3% decrease** in recommendation rate
- Chi-Square test confirmed workload category significantly impacts recommendation outcome (p < 0.001)

### 3. 📝 Grade Expectations Matter
- Students whose grades **met or exceeded expectations** showed higher recommendation rates (87.16% vs. 83.39%)
- Independent t-test confirmed this difference is statistically significant

### 4. 🏫 Smaller Classes Tend to Score Higher
- Small classes (20–94 students) averaged slightly higher recommendation rates than large classes (95–1,101 students)
- Weak negative correlation of **-0.074** — enrollment size alone explains only ~0.5% of variance
- Effect is real but modest; instructor quality dominates

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/qiwen-wen/UCSD-Course-Insights.git
cd UCSD-Course-Insights

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn statsmodels scipy patsy

# 3. Download the dataset and place it in data/CAPEs.tsv

# 4. Open the notebook
jupyter notebook FinalProject.ipynb
```

---

## 💡 Conclusions

Instructor quality emerged as the dominant factor in student course satisfaction, with a strong positive correlation across all STEM departments. While workload and grade expectations have measurable effects, they contribute far less to the overall recommendation rate. Class size shows a weak negative effect — smaller classes tend to perform better, though it is not a strong standalone predictor. These findings offer practical guidance for both students choosing courses and institutions looking to improve teaching effectiveness.

---

## 📌 Acknowledgements

- Data provided by [UCSD Historical Enrollment Data](https://github.com/UCSD-Historical-Enrollment-Data)
- Project completed as part of **COGS 108: Data Science in Practice** at UC San Diego (Winter 2025)
