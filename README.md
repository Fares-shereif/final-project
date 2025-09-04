# Student Performance Insights: From Cleaning to Clustering to Classification

**Author:** Fares Shereif Ismail  

---

## 📌 Overview
This project provides a comprehensive analysis of the **UCI Student Performance dataset**.  
The primary objective is to identify key factors influencing student academic performance and to develop predictive models that can identify **at-risk students**.  

The methodology encompasses a full data science workflow:
- Data cleaning  
- Exploratory data analysis (EDA)  
- Feature engineering  
- Unsupervised learning (K-Means clustering) for student profiling  
- Supervised machine learning for grade prediction  

The insights from this analysis can help educational institutions shift from a **reactive** to a **proactive** approach in supporting student success.

---

## 🔎 Methodology
The analysis follows a structured approach:

1. **Data Preparation**  
   - Dataset loaded, cleaned, and checked for inconsistencies  
   - Outliers handled using **IQR winsorization**  

2. **Exploratory Data Analysis (EDA)**  
   - Statistical summaries  
   - Correlation analysis  
   - Hypothesis testing  

3. **Feature Engineering**  
   - One-hot encoding for categorical features  
   - Scaling for numeric features  
   - New features created:  
     - `pass` (binary)  
     - `risk` (multi-class)  

4. **Unsupervised Learning**  
   - **K-Means clustering** applied to segment students into behavioral profiles:  
     - Dedicated  
     - Social  
     - At-Risk  

5. **Supervised Learning**  
   - Classification models trained:  
     - Logistic Regression  
     - Random Forest  
     - SVM  
   - Prediction tasks:  
     - Binary (pass/fail)  
     - Multi-class (risk level)  

---

## 📊 Results
- **Key predictors:** prior failures & absences  
- Students with **2+ failures** are **3x more likely to fail**  
- Models with **G1/G2 grades** → **96% F1-score**  
- Models **without G1/G2** → ~**80% F1-score** (useful for **early prediction**)  
- Clustering revealed **3 personas**:  
  - Dedicated  
  - Social  
  - At-Risk (**38% of students**, accounting for most failures)  

---

## ⚙️ Reproducibility Steps

### 1. Set Up the Environment
It is recommended to create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

## 2. Install Dependencies

Install required Python libraries:
```bash
pip install -r requirements.txt
```

## 3. Run the Jupyter Notebook

Open the provided notebook:
```bash
jupyter notebook Project.ipynb
```
## 4. Execute the Cells
- Run all cells sequentially to reproduce:
- Data loading & cleaning
- EDA
- Feature engineering
- Clustering
- Model training & evaluation




