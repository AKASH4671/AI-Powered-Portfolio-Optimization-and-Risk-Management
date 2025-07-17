# AI-Powered-Portfolio-Optimization-and-Risk-Management
**Merging AI, Convex Optimization, and Portfolio Theory for Smarter Investments**

## 📌 Overview  
This end-to-end project blends **Modern Portfolio Theory (MPT)** with **AI/ML techniques** to create smarter, more diversified portfolios and predict their performance. We move beyond traditional methods like Equal-Weighting by applying **Principal Component Analysis**, **Clustering**, and **LSTM Neural Networks** — all underpinned by a strong foundation in **portfolio optimization** and **risk-adjusted performance evaluation**.

---

## Objectives

- Construct optimal portfolios using both classical (Markowitz MPT) and AI-enhanced techniques.
- Analyze risk-adjusted performance (Sharpe, Sortino, Max Drawdown).
- Solve a convex optimization problem to find the Max Sharpe Portfolio.
- Evaluate diversification strategies using return predictability via LSTM.
- Compare outcomes of Naive, Clustered, and PCA-based portfolios.

---

## AI Meets Finance: Key Techniques

### 1️⃣ Portfolio Optimization (Core Foundation)
We start by applying Modern Portfolio Theory to:
- Simulate thousands of random portfolios
- Compute expected return, volatility, and Sharpe Ratio
- Plot the Efficient Frontier

Identified:
- Minimum Variance Portfolio  
- Maximum Sharpe Portfolio (via simulation and convex optimization)

✅ This created our **baseline for comparison** before AI enhancements.

---

### 2️⃣ Convex Optimization: Max Sharpe Portfolio  
We reformulated the Max Sharpe Ratio problem as a **convex optimization** task using `scipy.optimize` with constraints:
- Full capital deployment (weights sum to 1)
- Allow short-selling (weights can be negative)

✅ This gave us the **mathematically optimal risk-adjusted portfolio**, outperforming random simulations.

---

### 3️⃣ AI-Based Diversification Techniques

####  PCA (Principal Component Analysis)
- Identified dominant latent risk factors  
- Stocks with high PC1 loadings were given larger weights  
- Built the **PCA-Weighted Portfolio**

####  KMeans Clustering
- Clustered stocks using top 2 principal components  
- Formed 3 groups: Growth, Core, and Defensive  
- Created a **Cluster-Diversified Portfolio** by selecting representative stocks

####  Equal-Weighted Portfolio
- Constructed as a naive baseline with equal weights

---

##  Risk-Adjusted Performance Analysis

For each portfolio, we calculated:
- Annualized Return  
- Annualized Volatility  
- Sharpe Ratio  
- Sortino Ratio  
- Maximum Drawdown  

✅ Insights:
- **Convex Optimization Portfolio** and **PCA-Weighted Portfolio** offered superior risk-adjusted performance.
- Naive Equal-Weighted method underperformed across multiple metrics.

---
## Forecasting Future Returns with LSTM

Using historical portfolio returns:
- Trained individual **LSTM models** to forecast next-day returns
- Compared Predicted vs. Actual returns

| Portfolio              | Predicted Return | Actual Return | Absolute Error |
|------------------------|------------------|---------------|----------------|
| **PCA Weighted**        | 0.00179          | 0.00671       | 0.00491        |
| **Cluster Diversified** | 0.00168          | -0.00232      | 0.00400        |
| **Equal Weighted**      | -0.00060         | 0.00858       | 0.00918        |

✅ Observations:
- AI-based portfolios (PCA & Clustering) had more **predictable returns** and **lower uncertainty**.
- Naive approach showed **high error**, highlighting its volatility.

---

## AI in Finance: Insights & Possibilities

### Observations:
- AI can **systematically enhance diversification** using latent factors and clustering.
- Convex optimization provides a **robust benchmark** for portfolio structuring.
- LSTM adds a **forward-looking lens** to backtested strategies.

###  Possibilities:
- Dynamic rebalancing using PCA/cluster shifts  
- AI-enhanced factor investing  
- Blending ARIMA + LSTM for multi-horizon predictions  
- Reinforcement Learning for portfolio allocation
