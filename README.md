# 💹 Financial Analytics Project — Portfolio Optimization under Real-World Constraints

## 🎯 Objective
This project evaluates the **effect of real-world investment constraints** on the performance of the **Mean-Variance (MV)** portfolio optimization model, where inputs are estimated using historical data.  
The analysis examines how constraints—such as **no short-selling** and **minimum investment per asset**—affect portfolio performance, volatility, and risk-return trade-offs.

---

## 📚 Dataset
- **Source:** [Ken French’s Data Library — 25 Developed Markets Portfolios Formed on Size and Book-to-Market](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/Data_Library/tw_5_ports_developed.html)
- **Period:** July 1990 – March 2025  
- **Frequency:** Monthly  
- **Type:** Value-weighted average returns  
- **Why This Dataset?**
  - Represents 25 diversified global portfolios → ideal for applying portfolio constraints such as minimum investment (1/2N)  
  - Captures long-term developed market trends for realistic portfolio testing  
  - Well-established dataset for academic and applied financial analysis

---

## ⚙️ Methodology

### 1. Estimation Framework
- **Rolling Estimation Window:** 60 months (5 years)  
- **Rationale:** Balances recency and statistical stability in mean and covariance estimation

### 2. Portfolio Strategies
| Strategy | Description | Constraints |
|-----------|--------------|-------------|
| **MV** | Unconstrained Mean-Variance portfolio | Short-selling allowed |
| **NSMV** | No-Shorting Mean-Variance portfolio | All weights ≥ 0 |
| **MIMV** | Minimum Investment Mean-Variance portfolio | All weights ≥ 1/(2N) |

### 3. Evaluation Procedure
- **In-Sample:** Used full data range to estimate parameters and compute portfolios  
- **Out-of-Sample:** Re-estimated parameters monthly over a 60-month rolling window  
- **Target Expected Return:** Average of all asset mean returns (~0.7%)  

---

## 🧠 Execution & Tools
- Simulated monthly portfolio returns for each strategy  
- Computed realized **mean**, **variance**, and **standard deviation**  
- Visualized **risk–return trade-offs** using **mean–standard deviation diagrams**  
- **Tools Used:** `Python`, `Excel`, `NumPy`, `Pandas`, `Matplotlib`, `cvxpy`

---

## 📊 Results & Insights

| Evaluation | Strategy | Mean Return | Std Dev | Key Takeaway |
|-------------|-----------|-------------|----------|---------------|
| **In-Sample** | MV | 0.0069 | 0.0438 | Lowest volatility, stable performance |
|  | NSMV | 0.0069 | 0.0429 | Slightly higher volatility, moderate return |
|  | MIMV | 0.0070 | 0.0350 | Lower risk, robust in-sample performance |
| **Out-of-Sample** | MV | 0.0072 | 0.0401 | Lowest risk, robust generalization |
|  | NSMV | 0.0084 | 0.0443 | Highest return, higher risk |
|  | MIMV | 0.0082 | 0.0408 | Best risk–return balance |

> 💡 **Key Findings**
> - **NSMV** achieved the **highest out-of-sample return (~0.84%/month)**, showing that no-short-selling can improve realized performance.  
> - **MV** minimized risk (Std Dev ≈ 4%), ideal for risk-averse investors.  
> - **MIMV** offered the **best risk-return trade-off**, showcasing diversification benefits.  
> - **Out-of-sample returns** exceeded in-sample results, highlighting robustness.  

---

## 📈 Visualizations

| Visualization | Description | Link |
|----------------|-------------|------|
| 📊 **Mean–Standard Deviation Diagram** | Shows risk-return trade-off among portfolios | [View Plot](results/mean_std_plot.png) |
| 📈 **Portfolio Returns Comparison** | In-sample vs Out-of-sample performance | [View Plot](results/returns_comparison.png) |
| 🧩 **Portfolio Weights Over Time** | Dynamic allocation visualization | [View Plot](results/weights_plot.png) |

---

## 🚀 Quick Access

- 📘 **[View Full Report (PDF)](https://github.com/rittikad/Financial-Analytics/blob/main/Report/IB99L0_5594410.pdf)**  
- 💻 **[View Jupyter Notebook](https://github.com/rittikad/Financial-Analytics/blob/main/Code/IB99L0_5594410.ipynb)**  
- 📊 **[Explore Dataset (CSV)](https://github.com/rittikad/Financial-Analytics/blob/main/Data/Developed_25_Portfolios_ME_BE-ME.csv)**

---

## 🌍 Impact
This project demonstrates the ability to:
- Combine **quantitative modeling** with **financial interpretation**
- Apply **statistical estimation** and **optimization algorithms** to real-world data  
- Translate theoretical models into **actionable investment insights**
---

## 🛠️ Skills Showcased
`Python` · `Excel` · `Statistical Modeling` · `Portfolio Optimization` · `Analytical Thinking` · `Financial Data Analysis` · `Data Visualization`

---

## 📅 Timeline
- **Data Range:** July 1990 – March 2025  
- **Estimation Window:** 60 months rolling  
- **Evaluation:** In-sample and Out-of-sample performance

---

