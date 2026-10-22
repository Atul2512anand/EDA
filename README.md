# Titanic Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-F37626?logo=jupyter&logoColor=white)
![pandas](https://img.shields.io/badge/Data-pandas-150458?logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Visualisation-Plotly-3F4F75?logo=plotly&logoColor=white)

An exploratory data analysis of the Titanic dataset using pandas, Matplotlib, Seaborn, and Plotly. The notebook examines data quality, distributions, relationships, and the factors most strongly associated with passenger survival.

## Overview

This is the analysis stage that follows data loading and precedes model building. It answers practical questions:

- How complete is the dataset?
- Which features are skewed or contain outliers?
- How does survival differ by sex and passenger class?
- Which variables correlate with survival?
- What patterns should inform feature engineering?

The notebook is intentionally concise: eight cells, a small set of high-value plots, and observations written for a study workflow.

## Dataset

| Item | Value |
|---|---|
| Source | [Kaggle — Titanic Dataset (yasserh)](https://www.kaggle.com/datasets/yasserh/titanic-dataset) |
| File | `Titanic-Dataset.csv` |
| Shape | 891 rows × 12 columns |
| Target | `Survived` (0 = no, 1 = yes) |
| Overall survival rate | 342 / 891 = **38.4%** |

## What the Notebook Covers

1. **Setup** — install/import pandas, NumPy, Matplotlib, Seaborn, and Plotly.
2. **Load** — download the dataset through KaggleHub and preview it.
3. **Structure and quality**
   - `df.info()`
   - `df.describe(include="all").T`
   - missing-value counts
4. **Univariate distributions**
   - Age histogram with KDE and boxplot
   - Fare histogram with KDE and boxplot
5. **Multivariate relationships**
   - Seaborn pairplot of Age, Fare, Pclass, encoded Sex, and Survived
   - Correlation heatmap for the same numeric/encoded features
6. **Survival analysis**
   - survival rate by sex
   - survival rate by passenger class
   - fare distribution split by survival
7. **Interactive visualisation**
   - Plotly histogram of fare coloured by survival status

## Key Findings

| Finding | Result |
|---|---|
| Missing data | `Age` 177 missing, `Cabin` 687, `Embarked` 2 |
| Overall survival | 342 of 891 passengers (38.4%) |
| Survival by sex | Female **74.2%** (233/314) vs male **18.9%** (109/577) |
| Survival by class | 1st **63.0%** (136/216), 2nd **47.3%** (87/184), 3rd **24.2%** (119/491) |
| Fare | Strongly right-skewed, with high-value outliers |
| Age | Approximately normal with a small tail of older passengers |
| Correlations | Encoded sex and passenger class show the clearest relationships with survival |

These are descriptive results from the dataset, not causal claims. They motivate features such as sex, passenger class, fare, age, and family size for a later model.

## Getting Started

### Google Colab

1. Open `EDA.ipynb` in Colab.
2. Run all cells. The notebook downloads the dataset through `kagglehub`.
3. Interactive Plotly output renders inline.

### Local Jupyter

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux/macOS
source .venv/bin/activate

pip install pandas numpy matplotlib seaborn plotly kagglehub jupyter
jupyter notebook EDA.ipynb
```

If KaggleHub is unavailable, replace the download cell with:

```python
import pandas as pd
df = pd.read_csv("Titanic-Dataset.csv")
```

## Project Structure

```text
EDA/
├── EDA.ipynb                 # 8-cell analysis notebook
├── Titanic-Dataset.csv       # Raw dataset (891 × 12)
├── screenshot/               # Exported notebook figures
└── README.md
```

The `screenshot/` directory contains the visual outputs captured from the notebook run.

## Notes and Limitations

- Missing values are counted and visualised, not imputed; cleaning is handled in the separate data-preprocessing project.
- `Cabin` is too sparse for a simple category plot and is left as-is here.
- The correlation heatmap uses an encoded `Sex` column (`male = 0`, `female = 1`) and only a subset of features.
- No statistical significance tests or confidence intervals are reported.
- No model is trained in this notebook; it is an EDA stage only.

## Dataset Credit

The dataset is provided by Kaggle user **yasserh** and is based on the classic Titanic passenger dataset. See the Kaggle page for licensing and usage terms.

## Author

**Atul Anand**  
B.Tech–M.Tech (Cyber Security), National Forensic Sciences University  
GitHub: [@Atul2512anand](https://github.com/Atul2512anand)
