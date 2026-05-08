# 🎓 Student Performance Analysis – EDA

## 🔍 Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on a student performance dataset to identify the key factors affecting academic success.

The analysis explores how study habits, parental education, lifestyle choices, and failures influence student grades across multiple academic terms.

---

## 📁 Dataset Information
- Source: UCI / Kaggle – student-por.csv  
- Total Students: 649  
- Features: 33 Columns  

### Key Features Used
- Age  
- Gender  
- Study Time  
- Failures  
- Absences  
- Mother’s Education (Medu)  
- Father’s Education (Fedu)  
- Alcohol Consumption (Walc, Dalc)  
- Free Time  
- Romantic Relationship  
- Activities  
- G1 (Term 1 Grade)  
- G2 (Term 2 Grade)  
- G3 (Final Grade)  

- Dataset Type: Mixed (Numerical + Categorical)  
- Nature: Educational dataset with zero missing values  

---

## 🧹 Data Cleaning & Preprocessing

### ✅ Null Value Check
```python
df.isnull().sum()
```

- No missing values found in the dataset  

### 🔠 Feature Separation
- Categorical columns separated from numerical columns  
- Discrete numerical features converted into categorical/object types where required:
  - studytime  
  - traveltime  
  - failures  

### 📋 Outlier Detection
Implemented custom IQR-based outlier detection:
```python
Q1 - 1.5 × IQR
Q3 + 1.5 × IQR
```

Findings:
- 21 outliers detected in absences  
- 1 outlier detected in age  

### ⚙️ Preprocessing Pipeline
- StandardScaler for numerical features  
- OneHotEncoder for categorical variables  
- ColumnTransformer used for preprocessing  

---

## 📊 Exploratory Data Analysis

### 🔹 Univariate Analysis
- Grade distribution (G1, G2, G3)  
- Age distribution  
- Failure distribution  

### 🔹 Bivariate Analysis
- Study Time vs Grades  
- Alcohol Consumption vs Final Grade  
- Parental Education vs Performance  

### 🔹 Multivariate Analysis
- Correlation Heatmap  
- Feature relationship analysis  
- Academic performance trends across multiple factors  

---

## 📌 Key Insights

### 📖 Study Time vs Performance
- Students studying more performed significantly better  
- Failure rate reduced from:
```python
33.5% → 5.7%
```

→ Study time showed a positive correlation with final grades.

### 🔗 Grade Correlation
Strongest predictors of final grade (G3):
```python
G2 → G3 = 0.919
G1 → G3 = 0.826
```

→ Previous academic performance strongly predicts final results.

### 👨‍👩‍👦 Family Influence
- Mother’s education showed slightly stronger impact than father’s education  
- Higher parental education correlated with better student grades  

### 🍺 Lifestyle Impact
Higher alcohol consumption negatively impacted academic performance:
```python
Walc → G3 correlation = -0.18
```

Final grades decreased as alcohol consumption increased.

### ⚠️ Failure Analysis
Failures showed the strongest negative correlation with grades:
```python
r = -0.393
```

→ Students with repeated failures require early intervention.

### 📊 Grade Progression
Average grades improved across academic terms:
- G1 Mean = 11.40  
- G2 Mean = 11.57  
- G3 Mean = 11.91  

---

## 💡 Key Learnings

- Clean datasets still require proper feature understanding  
- Correlation analysis can reveal powerful predictive relationships  
- Lifestyle and study habits significantly affect student performance  
- Outlier detection is important even in educational datasets  
- EDA helps uncover actionable insights for academic improvement  

---

## 🛠️ Tools & Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  


Examples:
- Correlation Heatmap  
- Grade Distribution Charts  
- Study Time vs Grade Analysis  
- Alcohol Consumption vs Performance  
- Outlier Boxplots  

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/student-performance-eda.git
```

### 2️⃣ Install Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3️⃣ Run Jupyter Notebook
```bash
jupyter notebook
```

---

## 📌 Project Status
✅ Completed  
🔄 Open for improvements and feedback  

---

## 🤝 Connect With Me
I’m currently learning Data Analytics and building real-world projects.


## ⭐ If You Found This Useful
Give this repository a star ⭐ and share your feedback!
