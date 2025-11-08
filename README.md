# Data-Science-Project1-Success-By-Majors-
Data analysis and machine learning project exploring how academic majors, performance metrics, and economic factors influence student success and GDP outcomes.

# 🎓 Math 237 Project 1 – Student Success and Economic Outcomes

This project investigates how **university majors**, **academic performance**, and **economic factors** (like GDP, inflation, and unemployment rate) relate to **student success and economic performance**.  
Developed in **Google Colab** using Python, Pandas, Seaborn, and Scikit-learn.

---

## 🧠 Project Goals

- Identify which majors are most likely to lead to student success or dropouts.
- Understand how academic features (grades, course load, tuition status) relate to success.
- Explore how external economic conditions (GDP, unemployment, inflation) interact with academic outcomes.
- Predict **GDP** using multiple academic and economic features through regression modeling.

---

## 📊 Dataset

The dataset (`data.csv`) contains student information, course codes, grades, enrollment details, and macroeconomic indicators.  
Each record represents an individual student with features such as:

- `Course`
- `Admission grade`
- `Age at enrollment`
- `Curricular units 1st/2nd sem (grade, approved, enrolled)`
- `Unemployment rate`
- `Inflation rate`
- `GDP`
- `Target` (Graduate, Dropout, Enrolled)

---

## 🔍 Exploratory Analysis

Key visualizations include:
- 📈 **GDP Distribution by Course**
- 📉 **Unemployment Rate by Course**
- 🚪 **Dropout Rate by Course**
- 🎓 **Graduate Success Rate by Course**
- 🔥 **Correlation Heatmap** — shows relationships among academic and economic features
- 📘 **Average Grade by Major**
- 🧩 **Actual vs Predicted GDP Plot** — visualizes model fit

These plots reveal how academic performance and external conditions correlate with student outcomes and overall economic performance.

---

## 🧮 Modeling Approach

### 1️⃣ Data Preprocessing
- Removed missing and infinite values
- One-hot encoded categorical variables
- Scaled numerical features with `StandardScaler`
- Created new engineered features:
  - `Grade_Difference` – difference between 2nd and 1st semester grades
  - `Avg_Grade` – average of both semester grades
  - `Approval_Ratio` – approved / enrolled units

### 2️⃣ Regression Models
A **multiple linear regression** model was used to predict GDP based on academic and economic factors.

#### Improved Model:
- After feature engineering and log-transforming GDP:
  - R² = **0.416**
  - Meaning ~41.6% of GDP variation is explained by academic and economic variables.

---


|  Linear Regression (log + features) | **0.416** | Stronger correlation, interpretable |

## 🧩 Key Insights

- Some majors consistently show higher success and lower dropout rates.
- Academic performance (grades, approvals) strongly correlates with success outcomes.
- GDP and unemployment interact with student performance, indicating broader economic influence.
- Success is **multifactorial**, not determined by major alone — academic and economic factors both matter.

---

## 🧰 Tech Stack

- **Python**  
- **Pandas** – data manipulation  
- **NumPy** – numerical processing  
- **Matplotlib & Seaborn** – visualization  
- **Scikit-learn** – machine learning models  
- **Google Colab** – development environment  

---

## 🚀 How to Run

1. Open the notebook in Google Colab.
2. Mount your Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')

3. paste this into a cell (change the file path name if necessary) and run: 

   ```python
   data = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/data.csv', sep=';')

