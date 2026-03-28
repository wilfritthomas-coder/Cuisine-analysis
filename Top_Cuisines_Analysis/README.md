# 🍽️ Top Cuisines Analysis

## Project Overview

This project analyses a restaurant dataset to identify the **three most dominant cuisines** and quantify their prevalence across all listed establishments. It is part of a data analytics internship task focused on deriving actionable insights from real-world restaurant data.

---

## 📁 Folder Structure

```
Top_Cuisines_Analysis/
│
├── Top_Cuisines_Analysis.ipynb   ← Main analysis notebook (step-by-step)
├── Dataset___2_.csv              ← Source dataset (9,551 restaurant records)
├── top_cuisines_results.csv      ← Exported results table (Top 3 cuisines)
├── top_cuisines_bar.png          ← Bar chart visualisation
├── top_cuisines_donut.png        ← Donut chart visualisation
├── Task_Explanation.txt          ← Plain-language explanation of the task
└── README.md                     ← Project documentation (this file)
```

---

## 🎯 Task Objective

- Determine the **top three most common cuisines** in the dataset.
- Calculate the **percentage of restaurants** that serve each of the top cuisines.

---

## 📊 Dataset Summary

| Property | Detail |
|----------|--------|
| Total Records | 9,551 rows |
| Valid Records (after cleaning) | 9,542 rows |
| Total Columns | 21 |
| Key Column Analysed | `Cuisines` |
| Missing Values in Cuisines | 9 (excluded from analysis) |

---

## 🔍 Methodology

1. **Load** the dataset using `pandas`.
2. **Clean** by removing rows where the `Cuisines` field is null.
3. **Split** multi-cuisine entries (comma-separated values) into individual cuisine tokens.
4. **Explode** the resulting list into individual rows for accurate frequency counting.
5. **Count** occurrences of each unique cuisine using `value_counts()`.
6. **Calculate** each top cuisine's percentage relative to total valid restaurant records.
7. **Visualise** results using bar and donut charts.
8. **Export** the summary table to CSV.

> **Important Note:** A single restaurant may offer multiple cuisines (e.g., "Chinese, Indian, Fast Food"). Percentages therefore represent the proportion of restaurants that include that cuisine among their offerings — totals may exceed 100%.

---

## 🏆 Key Results

| Rank | Cuisine | Restaurant Count | Percentage |
|------|---------|:---------------:|:----------:|
| 🥇 1 | North Indian | 3,960 | 41.50% |
| 🥈 2 | Chinese | 2,735 | 28.66% |
| 🥉 3 | Fast Food | 1,986 | 20.81% |

---

## 📈 Visualisations

### Bar Chart — `top_cuisines_bar.png`
A vertical bar chart displaying the absolute count of restaurants serving each of the top three cuisines, annotated with count and percentage labels.

### Donut Chart — `top_cuisines_donut.png`
A donut chart illustrating the proportional share of each top cuisine among all valid restaurant records, with the total restaurant count displayed in the centre.

---

## 🛠️ Requirements

```
Python  >= 3.8
pandas  >= 1.3
matplotlib >= 3.4
seaborn >= 0.11
```

Install dependencies:
```bash
pip install pandas matplotlib seaborn
```

---

## ▶️ How to Run

1. Ensure `Dataset___2_.csv` is in the same directory as the notebook.
2. Open `Top_Cuisines_Analysis.ipynb` in **Jupyter Notebook** or **JupyterLab**.
3. Run all cells sequentially (`Kernel → Restart & Run All`).
4. Outputs (charts and CSV) will be saved in the same folder automatically.

---

## 📌 Insights & Takeaways

- **North Indian cuisine** is overwhelmingly the most prevalent, appearing in over **4 in 10 restaurants** — reflecting strong cultural and consumer preference for this cuisine type.
- **Chinese cuisine** maintains a strong second position, present in nearly **3 in 10 restaurants**, indicating broad mainstream appeal.
- **Fast Food** rounds out the top three at just over **1 in 5 restaurants**, consistent with global trends in quick-service dining growth.

---

*Analysis conducted as part of a Data Analytics Internship Programme.*
