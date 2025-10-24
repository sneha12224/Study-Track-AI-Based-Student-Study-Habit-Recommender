# Student Performance EDA Project

# Overview
This project explores and analyzes the Student Performance dataset. It covers data loading, cleaning, merging, preprocessing, and exploratory data analysis (EDA) using Python and pandas in Google Colab.

## Objective
Perform data preprocessing and Exploratory Data Analysis (EDA) on a students dataset split into two related tables:
- 'Milestone1_EDA.ipynb' — Main analysis notebook
- `table1.csv` — Students information
- `table2.csv` — Study_Logs (weekly study hours and focus logs)

## Steps followed
1. **Load tables**: Read `table1.csv` (students) and `table2.csv` (study logs). If `table2.csv` is missing, the notebook creates a synthetic one.
2. **Join**: Used `pandas.merge()` on `student_id` to combine study logs with student information.
3. **Preprocess**:
   - Handle missing values (impute numeric with median, categorical with mode).
   - Drop duplicates.
   - Convert data types (`date` to datetime).
   - Encode categorical variables (Label Encoding and one-hot encoding for parental education).
   - Scale numeric features (StandardScaler) and save scaled columns.
4. **Descriptive analysis**:
   - Summary statistics (count, mean, std, min, max, median).
   - Correlation matrix between scores and study variables.
   - Outlier detection using IQR method.
5. **EDA / Visualizations**:
   - Distribution histogram + KDE for math scores.
   - Boxplot of math score by test preparation course.
   - Scatter plot (study hours vs math score) with trendline.
   - Correlation heatmap.
6. **Save output**: Cleaned and merged dataset saved in `Milestone1_output/merged_cleaned.csv`.

## Tools used
- Python (Pandas, NumPy)
- Matplotlib & Seaborn for visualizations
- scikit-learn for encoding & scaling
- Google Colaboratory (.ipynb)

## Key insights (example)
- Strong positive correlations between `math score`, `reading score`, and `writing score` (students who perform well in one tend to do well in others).
- Study hours show a modest positive correlation with math score (visualized in scatter plot).
- Outliers detected in `study_hours` and test scores—investigate log entries for data-entry errors or exceptional cases.
- Test preparation course often associates with higher median scores (visible in boxplot).

## How to run
1. Open `Milestone1_EDA.ipynb` in Google Colab.
2. Upload `data/table1.csv` into the `data/` folder in Colab, or upload directly through Colab's upload UI.
3. Run the cells in order. The notebook will create `data/table2.csv` if it is missing.
4. View figures inline; the merged cleaned CSV is saved to `Milestone1_output/merged_cleaned.csv`.
