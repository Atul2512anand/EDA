# 🧠 Titanic Dataset – Exploratory Data Analysis (EDA)

This project performs **Exploratory Data Analysis (EDA)** on the Titanic dataset using `Pandas`, `Matplotlib`, `Seaborn`, and `Plotly`. It is part of Task 2 in a structured data science pipeline focused on understanding the dataset through visual and statistical techniques.

---

## 🎯 Objective

To understand the Titanic dataset using:
- Summary statistics (mean, median, std, etc.)
- Visualizations like histograms, boxplots, correlation heatmaps, and pairplots
- Feature-level relationships and patterns
- Basic inferences to guide further analysis or machine learning

---

## 📁 Dataset

- **Source**: [Kaggle – Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)
- **File Used**: `Titanic-Dataset.csv`

---

## 📊 EDA Tasks Performed

### 1. Summary Statistics
- Dataset info, missing values
- Central tendency: mean, median, std, min, max

### 2. Visualizations
- **Histograms** and **Boxplots** for:
  - Age
  - Fare
- **Bar Charts** for:
  - Survival rate by Sex
  - Survival rate by Pclass
- **Pairplot** for relationships between multiple features
- **Correlation Matrix** with a heatmap

### 3. Interactive Plotly Charts
- Fare distribution by survival status

---

## 🔍 Key Observations

| Feature       | Inference |
|---------------|-----------|
| `Sex`         | Females had a much higher survival rate. |
| `Pclass`      | 1st class passengers were more likely to survive. |
| `Fare`        | Higher fare generally correlated with survival. |
| `Age`         | Slight trend: children had slightly better odds. |
| `Sex + Pclass`| Strong correlation with survival outcome. |

---

## 📦 Tools Used

- `Pandas` for data manipulation
- `Matplotlib` & `Seaborn` for visualizations
- `Plotly` for interactive graphs
- `Google Colab` as the development environment

---

## 📝 How to Run

1. Clone this repository or open the notebook in Google Colab.
2. Upload the `Titanic-Dataset.csv` file when prompted.
3. Run the cells to see all graphs and insights.

---

## 📂 Folder Structure

Task-2-EDA/
├── Titanic-Dataset.csv
├── EDA_Titanic.ipynb
├── README.md
└── screenshots/


---

## ✅ Status

> 📌 Task 2: EDA Completed  
> 🔜 Next: Task 3 – Machine Learning Model Building

---

## 🙌 Contributions

Made by **Atul Anand** as part of a hands-on learning project on data preprocessing and analysis.

---

## 📌 License

This project is for educational purposes. Dataset © [Kaggle](https://www.kaggle.com/) under respective license.

