# Study-Track-AI-Based-Student-Study-Habit-Recommender

## Project: AI-Based Student Study Habit Recommender Track: Infosys Study Track – AI-Based Student Study Habit Recommender

🎯 Objective

The goal of this milestone is to prepare a clean and analysable dataset by performing data preprocessing and exploratory data analysis (EDA). This ensures a solid foundation for building a recommendation model that suggests personalized study habits for students.

🧩 Dataset Description

Dataset Source: Kaggle Student Performance Dataset

We used two related tables:

Maths.csv – Contains demographic, social, and school-related information for students studying Mathematics.

Portuguese.csv – Contains similar data for students studying Portuguese.

Common Key: school, sex, age, and address (used to merge both datasets logically).

⚙️ Steps Followed

Data Loading & Joining
Imported both datasets using Pandas.

Merged datasets into one consolidated dataframe using pd.merge() on common keys.

Data Preprocessing
Handled missing values: Filled or dropped as appropriate.

Removed duplicates: Ensured unique student records.

Fixed data types: Converted numeric and categorical columns correctly.

Encoded categorical variables: Used LabelEncoder() for gender, address type, etc.

Normalized numeric columns (optional): Applied MinMaxScaler() for uniformity.

Descriptive Analysis
Calculated key statistics using df.describe() and .info().

Identified correlations between academic performance and study-related habits.

Detected outliers using IQR and boxplots.

Exploratory Data Analysis (EDA)
Created visual insights using Matplotlib and Seaborn:

📊 Distribution Plot: Study time and final grade distribution.

🧩 Scatter Plot: Relationship between absences and final grades.

🔥 Correlation Heatmap: Highlights correlations among numerical features.

📈 Bar Plot: Comparison of grades by gender and parental education.

🧰 Tools & Libraries Used

Python

Google Colaboratory

Pandas – Data loading, cleaning, joining

Matplotlib & Seaborn – Visualization and pattern detection

NumPy – Numeric operations

Scikit-learn (optional) – Encoding and scaling
