# Titanic-Dataset-Exploratory-Data-Analysis-EDA-
# Titanic Dataset EDA — Syntecxhub Internship (Project 3)

This repository contains my third project for the Syntecxhub Data Science Internship.
The goal of this task was to perform a structured exploratory data analysis (EDA) on
the Titanic dataset to understand survival patterns based on key passenger features.

---

## 🔍 Project Goals
- Explore dataset structure and missing values
- Analyze survival patterns by:
  - Sex
  - Passenger Class
  - Age Groups (via custom AgeBucket feature)
- Create visualizations for survival trends
- Summarize insights with clear interpretation

---

## 📊 Key Findings
- Female passengers had significantly higher survival rates than males.
- 1st-class passengers survived much more frequently than 3rd-class.
- Survival increased progressively from teens → adults → middle-aged passengers.
- Passenger demographics and ticket class were the strongest survival indicators.

---

## 🛠 Tools & Libraries
- Python 3
- Pandas
- NumPy
- Seaborn
- Matplotlib
- VS Code

---

## 📂 Repository Structure
Syntecxhub_Titanic_EDA/
│── eda.py
│── titanic.csv
│── README.md
└── outputs/
    ├── survival_by_sex.png
    ├── survival_by_class.png
    └── survival_age_violin.png

---

## ▶ How to Run
```bash
pip install pandas seaborn matplotlib
python eda.py
