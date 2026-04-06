# 📊 Statistical Revenue Analysis: Megaline Prepaid Plans (Surf vs. Ultimate)

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-150438?style=for-the-badge&logo=matplotlib&logoColor=black" />
</p>

## 📌 Project Overview
This project acts as a data-driven consultancy for the telecom operator **Megaline**. The primary objective was to analyze the behavior of 500 customers and determine which prepaid plan—**Surf** or **Ultimate**—generates more revenue. The findings serve as a strategic base for the commercial department to optimize the annual advertising budget.

## 🛠️ Key Methodologies
* **Data Engineering:** Aggregation of call logs, SMS, and web traffic into a consolidated "user-month" unit of analysis.
* **Business Logic Implementation:** Applied Megaline's specific billing rules (rounding seconds to minutes and megabytes to gigabytes).
* **Statistical Inference:**
    * **Welch's T-Test:** Used for revenue comparison between plans due to significantly unequal variances.
    * **Levene's Test / Variance Analysis:** Conducted to ensure the robustness of the hypothesis testing parameters.
    * **Outlier Detection:** Identification of "heavy users" in the Surf plan using the Interquartile Range (IQR) and 95th percentile thresholds.

## 📈 Final Insights & Decision
The analysis highlighted that while the Surf plan has a lower entry cost, the Ultimate plan provides a more stable and higher average return:

| Metric | Surf Plan (Avg) | Ultimate Plan (Avg) | Statistical Significance |
| :--- | :--- | :--- | :--- |
| **Monthly Revenue** | **$60.71** | **$72.31** | ✅ Significant (p < 0.05) |
| **Revenue Stability** | ❌ Volatile (High Overages) | ✅ Highly Predictable | N/A |
| **Data Usage** | ~18 GB (Above Limit) | ~18 GB (Below Limit) | ❌ No significant diff. |

### 🎯 Final Recommendation: **FOCUS ON ULTIMATE PLAN**
**Strategic Verdict:** The **Ultimate Plan** is the most profitable for Megaline. Although some Surf users generate high revenue through overages (reaching up to $600), the Ultimate plan offers a higher LTV (Lifetime Value) with lower volatility. Marketing efforts should prioritize the Ultimate plan to guarantee a stable and superior revenue stream.

## 📂 Repository Structure
* `/datasets`: Anonymized data for calls, internet, messages, plans, and users.
* `/notebooks/notebook.ipynb`: Full Python implementation, data cleaning, and statistical validation.
