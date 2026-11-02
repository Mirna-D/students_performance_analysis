# 📊 Student Performance Analysis & Academic Insights

![Project Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
![Domain](https://img.shields.io/badge/Domain-Education_Analytics-blue?style=flat-square)
![Tools](https://img.shields.io/badge/Tools-Google_Sheets%2FExcel%20%7C%20SQL-orange?style=flat-square)

An exploratory data analysis (EDA) case study analyzing the impact of socioeconomic factors (lunch subsidies), test preparation course completion, and parental educational background on students' academic performance across 1,000 student records.

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Architecture](#-dataset-architecture)
- [Methodology & Data Preparation](#-methodology--data-preparation)
- [Key Insights & Findings](#-key-insights--findings)
- [Data Visualizations](#-data-visualizations)
- [Strategic Recommendations](#-strategic-recommendations)
- [Repository Structure](#-repository-structure)
- [How to Use](#-how-to-use)
- [Author & Contact](#-author--contact)

---

## 🎯 Project Overview

Understanding the underlying drivers of student performance allows educational institutions to allocate resources effectively and implement targeted intervention programs. 

This project aims to:
**analyzing the factors that influence students' academic performance.**

---

## 🗃️ Dataset Architecture

* **Source:** [Kaggle - Student Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
* **Size:** 1,000 records × 8 columns

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `gender` | Categorical | Student gender (`female`, `male`) |
| `race/ethnicity` | Categorical | Demographic grouping (`Group A` to `Group E`) |
| `parental level of education` | Categorical | Parent's highest degree attained (6 levels) |
| `lunch` | Categorical | Lunch type standard vs free/reduced (socioeconomic proxy) |
| `test preparation course` | Categorical | Completion status (`none`, `completed`) |
| `math score` | Numerical | Math test score (0 - 100) |
| `reading score` | Numerical | Reading test score (0 - 100) |
| `writing score` | Numerical | Writing test score (0 - 100) |

---

## 🧹 Methodology & Data Preparation

1. **Data Cleaning & Auditing:**
   - Checked for missing values across all 1,000 rows (0 missing found).
   - Scanned for duplicate entries and outliers (scores bounded cleanly between 0 and 100).
   - Verified category value consistency (case sensitivity & whitespace cleaning).

2. **Feature Engineering:**
   - Derived `Average Score` calculated as `(math score + reading score + writing score) / 3`.

3. **Data Aggregation:**
   - Utilized Pivot Tables to calculate cross-tabulated averages across `lunch` and `test preparation course`.

---

## 💡 Key Insights & Findings

### 1. The Combined Effect (16.6 Point Swing)
Students with **standard lunch** who **completed the test preparation course** achieved the highest overall average score (**75.5**). Conversely, students with **free/reduced lunch** who **did not take the course** scored the lowest (**58.9**).

| Lunch Subsidies | Test Prep Status | Average Score |
| :--- | :--- | :---: |
| **Standard** | **Completed** | **75.5** 🥇 |
| **Standard** | None | 68.3 |
| **Free / Reduced** | **Completed** | 67.8 |
| **Free / Reduced** | None | **58.9** 🔻 |

> **Key takeaway:** Having access to test preparation offsets the socioeconomic disadvantage, raising free/reduced lunch students' average scores to 67.8 (nearly matching standard lunch students without prep at 68.3).

### 2. Parental Education Influence
There is a direct positive correlation between parents' education level and student performance:
* **Master's Degree:** 73.6 Avg Score
* **Bachelor's Degree:** 71.9 Avg Score
* **High School:** 63.1 Avg Score

---

## 📈 Data Visualizations

### Combined Effect: Lunch vs. Test Prep Course
```
Standard + Completed     [===========================] 75.5
Standard + None          [=====================] 68.3
Free/Reduced + Completed [====================] 67.8
Free/Reduced + None      [=================] 58.9
                         +---------+---------+---------+
                         0        25        50        75
```

---

## 💡 Strategic Recommendations

1. **Curriculum Integration:** Integrate core test preparation modules into the regular school curriculum or mandate enrollment for students performing below average.
2. **Targeted Subsidies:** Shift funding from general subsidies to targeted subsidies—providing 100% free test prep course registration for all students receiving free/reduced lunch.
3. **Parent Engagement:** Establish parent-school engagement initiatives and targeted tutoring programs specifically tailored for students whose parents have lower educational backgrounds.

---

## 📂 Repository Structure

```text
├── data/
│   ├── (RAW) StudentsPerformance.xlsx       # Original dataset from Kaggle
├── analysis/
│   └── (DA) StudentPerformance.csv      # Pivot tables & aggregation sheets
└── README.md                               # Project documentation
```

---

## 🛠️ How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/Mirna-D/student_performance_analysis.git
   ```
2. Open `analysis/(DA) StudentsPerformance` in Microsoft Excel or Google Sheets to inspect the pivot tables and charts.

---

## 👤 Author & Contact

**Mirnawati Darwis**
* **Role:** Data Analyst & Data Scientist
* **LinkedIn:** [linkedin.com/in/mrnaad](https://linkedin.com/in/mrnaad)
* **GitHub:** [@Mirna-D](https://github.com/Mirna-D)
* **Email:** meetellmee@gmail.com