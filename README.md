# Capstone-Project
# 🎓 The Chronicles of Higher Education

**A Data-Driven Investigation of Waitlist Trends Across R1 Universities (2018–2022)**  
*By Raasikh Naveed | Wichita State University | Capstone Project*

---

## 📘 Overview

This project explores how university waitlist practices have evolved over the past five years, with a key focus on **Fall 2020**, the academic cycle most affected by the **COVID-19 pandemic**. Using data collected from over 50 R1 universities, this analysis highlights significant changes in waitlist admissions, models predictive trends using machine learning, and provides actionable insights for institutions and students alike.

---

## 🎯 Objectives

- Analyze year-over-year waitlist statistics (2018–2022)
- Identify trends and outliers in waitlist offers and acceptances
- Forecast waitlist behavior using advanced ML models
- Compare linear and non-linear approaches (ARIMA vs LSTM)
- Explore the impact of COVID-19 on university enrollment behavior

---

## 📊 Dataset

- **Total Universities Considered:** 147 R1 universities  
- **Clean Dataset:** 287 rows × 5 columns  
- **Final Sample:** 57 universities with complete waitlist data across 5 years  
- **Missingness:**  
  - 63 universities didn’t disclose waitlist info  
  - 27 had ≥3 years of missing data

---

## 🧪 Methodology

### 📌 Data Preparation

- Cleaned and normalized missing values
- Applied **99th percentile capping** to handle outliers (especially 2022 anomalies)
- Separated yearly datasets for individual modeling

### 🔍 Exploratory Analysis

- Compared waitlist activity pre-, during-, and post-pandemic
- Identified a **55.1% increase** in admitted students from the waitlist in Fall 2020
- Visualized institution-specific patterns in response to enrollment shifts

---

## 🧠 Modeling Techniques

### 🔷 LSTM (Long Short-Term Memory)

- Built using Keras Sequential API  
- Captures long- and short-term temporal trends  
- Trained on 3 years, tested on 2  
- ✅ **Best performer**

**📈 LSTM Predictions:**
- 2022 Actual: 5456 | Predicted: 5484.5
- 2023: 5484.52
- 2024: 5290.13
- 2025: 5140.37
- 2026: 4992.01

---

### 🔶 ARIMA & SARIMA

- ADF Test confirmed stationarity (p-value: 5.63e-11)
- Parameters selected: p ∈ [1,3], q = 5, d = 0
- **Drawback:** Predictions were overly smooth and failed to capture variability

> “Linear models like ARIMA/SARIMA struggled to reflect the complex, nonlinear behavior of post-COVID waitlist fluctuations.”

---

## 📌 Key Findings

- Waitlist offers surged in **2020** due to enrollment uncertainty
- Post-2020, a **decline** suggests universities regained forecasting confidence
- Budget and department size influenced university-level decisions
- **University of Michigan** & **CMU** used waitlists strategically in STEM  
- **Berkeley** showed reduced movement in humanities due to budget cuts

---

## 💡 Recommendations

### For Universities
- Increase transparency in waitlist policies and historical data
- Use advanced ML (e.g., LSTM) for admission forecasting
- Monitor department-level trends to optimize offers
- Balance equity and efficiency in decision-making

### For Students
- Research program-specific waitlist behavior
- Communicate with admissions offices early
- Prepare backup plans in case of deferred or waitlist outcomes

---

## 🛠 Tech Stack

- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Keras)
- Time Series Models: LSTM, ARIMA, SARIMA
- Jupyter Notebooks
- Microsoft Excel for initial data wrangling
- PowerPoint for visual storytelling

---

## 🧭 Roadmap

- [ ] Launch interactive dashboard (Streamlit / Tableau)
- [ ] Integrate more R1 data for 2023–24
- [ ] Build a comparative model using GRUs or Transformer-based time series
- [ ] Write a Medium/LinkedIn blog post (in progress 😉)

---

## 📚 References

- [The Michigan Daily – Waitlist Frustration in CS](https://www.michigandaily.com/news/academics/students-discuss-frustrations-long-waitlists-upper-level-computer-science-classes/)
- [EdSource – CSU Budget Cuts](https://edsource.org/2024/budget-cuts-begin-to-surface-at-california-state-university/718699)
- [CMU – MS in AI and Innovation](https://msaii.cs.cmu.edu/)

---

## 🙋‍♂️ About the Author

**Raasikh Naveed** is a Data Science graduate student at Wichita State University with a passion for turning real-world educational challenges into analytical opportunities. This capstone project is part of his pursuit to apply machine learning in higher education and policy analysis.

---

## 📬 Questions?

Feel free to open an issue or reach out via [LinkedIn](https://www.linkedin.com/in/raasikhnaveed).

