# Data Analysis — Food Products Dataset (Course 2 Project)

A comprehensive data analysis course project working with a large-scale food product dataset (~385 K rows). The work progresses from raw data ingestion through cleaning, exploratory analysis, NLP text processing, time-series inspection, and advanced statistical tests.

---

## Project Structure

```
data_analysis-main/
├── Course2_Project_Report.ipynb   ← main Jupyter notebook (all 7 tasks, ~214 cells)
├── README.md                      ← project documentation (this file)
└── data_385k.pkl                  ← compressed dataset (~385 K food products; not in repo)
```

### Notebook Layout (`Course2_Project_Report.ipynb`)

| Task | Title | Key Steps |
|------|-------|-----------|
| **A** | An overview of the dataset | Load pickle file; inspect shape, dtypes, sample rows; group columns by suffix (`_per_hundred`, `_per_portion`, `_unit`, other) |
| **B** | Data Cleaning | Detect & remove duplicate rows; build missing-value count/percentage table; visualise missing data with `missingno` |
| **C** | Preliminary EDA | Range / physics-based validation; z-score & threshold outlier detection; distribution plots (histograms, box plots) |
| **D** | EDA — Text data | NLP cleaning & lemmatisation (`WordNetLemmatizer`); ingredient tokenisation; top-ingredient frequency bar charts |
| **E** | EDA — Time-series data | Parse `created_at` timestamps; monthly/yearly product-creation heatmaps |
| **F** | EDA — Correlation analysis | Pearson correlation heatmap; chi-squared test of independence between categorical variables |
| **G** | Advanced EDA | Organic vs non-organic classification; violin plots comparing nutrient distributions across product groups |

---

## Dataset

| Property | Detail |
|----------|--------|
| File | `data_385k.pkl` (compressed pickle — not included in repo) |
| Rows | ~385 000 food products |
| Languages | English, French, German product names & ingredients |
| Countries | Multiple (US, FR, DE, UK, AT, …) |
| Key columns | `product_name_en/fr/de`, `ingredients_en`, `country`, `created_at`, `energy_per_hundred`, `energy_kcal_per_hundred`, macronutrient and micronutrient `_per_hundred` / `_per_portion` columns |

---

## Setup & Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn missingno scipy nltk
python -c "import nltk; nltk.download('stopwords'); nltk.download('wordnet')"
```

---

## Key Concepts Covered

| Concept | Task |
|---------|------|
| Data loading & inspection | A |
| Duplicate & missing-value handling | B |
| Range / physics-based data validation | C |
| Outlier detection (z-score, manual thresholds) | C |
| NLP text cleaning & lemmatisation | D |
| Ingredient frequency analysis | D |
| Time-series heatmaps | E |
| Correlation analysis | F |
| Chi-squared test of independence | F |
| Organic vs non-organic product classification | G |
| Violin plot distribution comparisons | G |
