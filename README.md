# Workforce Attrition Analytics Dashboard

> Data Analytics project combining SQL cost modelling, business insight
> analysis, and a 5-view Tableau dashboard for HR attrition intelligence.

## Live Dashboard

**Tableau Public**: https://public.tableau.com/views/WorkforceAttritionDashboard/WorkforceAttritionDashboard

## Key Insights

- **Overtime = 3x attrition risk**: Employees on overtime leave at 30.5% vs
  10.4% for non-overtime - confirmed across SQL analysis and Tableau visual
- **$57M replacement exposure**: Total cost-of-attrition across all departments
  using industry benchmark of 50% annual salary per departure
- **R&D paradox**: Despite lowest attrition rate (13%), R&D carries the highest
  replacement cost ($36M) due to higher average salaries
- **Early tenure danger**: 0-2 year employees leave at 35% - highest of any
  tenure band, pointing to onboarding as root cause

## Dashboard Views

| View | Insight |
|------|---------|
| Attrition Heatmap | Department x JobRole grid - Sales Reps at 39.8% |
| Cost of Attrition | Replacement cost by department - R&D leads at $36M |
| Risk Distribution | 123 High / 525 Medium / 822 Low risk employees |
| Income vs Risk Scatter | Low income + overtime = highest risk cluster |
| Attrition Drivers | Overtime, satisfaction, tenure benchmarked vs 16.1% avg |

## SQL Analytics (8 queries)

| Query | Finding |
|-------|---------|
| Attrition by department | Sales 20.6%, HR 19.0%, R&D 13.8% |
| Attrition by job role | Sales Representatives 39.8% |
| Overtime effect | 30.5% vs 10.4% - 3x multiplier |
| Tenure band analysis | 0-2 years: 35% attrition |
| Income quartile | Bottom quartile: 26% vs top quartile: 8% |
| Overtime x satisfaction | Combined: 46% attrition rate |
| Cost of attrition | $57M total replacement exposure |
| Early tenure churn | Peak attrition at year 1 |

## Tech Stack

| Tool | Purpose |
|------|---------|
| SQL (SQLite) | Analytics queries + cost model |
| pandas | Data preparation + export |
| Tableau Public | 5-view interactive dashboard |
| Python | Scoring pipeline + CSV exports |

## Notebooks

| Notebook | What it does |
|----------|-------------|
| 01_Week1_EDA_SQL | EDA + 8 SQL analytics queries + cost model |
| 08_Tableau_Export | Scores all employees, exports 6 dashboard CSVs |

## Dataset

IBM HR Analytics Employee Attrition
- Source: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

## How to Run
```bash
conda create -n attrition python=3.10 -y
conda activate attrition
pip install pandas numpy scikit-learn lightgbm joblib
```

1. Download IBM dataset from Kaggle -> place in /data folder
2. Run 01_Week1_EDA_SQL.ipynb for SQL analytics
3. Run 08_Tableau_Export.ipynb to generate dashboard CSVs
4. Open Tableau Public -> connect to dashboard/employees_master.csv

## Resume Bullet

Built workforce attrition analytics system - 8 SQL queries on SQLite
identifying overtime as 3x attrition driver, cost-of-attrition model
quantifying $57M replacement exposure, and 5-view Tableau dashboard
(heatmap, cost analysis, risk distribution, income-risk scatter, drivers
chart) published at Tableau Public.
