---
alias: 🔬ZhaZ21
cite: "Zhang, Zihao, Stefan Zohren, and Stephen Roberts. “Deep Learning for Portfolio Optimization.” _The Journal of Financial Data Science_ 2, no. 4 (November 2, 2020): 8–20. [https://doi.org/10.3905/jfds.2020.1.042](https://doi.org/10.3905/jfds.2020.1.042)."
---

# Summary
- Return forecasting approach is not guaranteed to maximize the performance of a portfolio
- Bypass the forecasting step to directly obtain asset allocations, by optimizing the [[Sharpe Ratio|Sharpe ratio]]

# Methodology

## Objective Function
$$
L = \frac{E[R_p]}{std[R_p]}
$$
where $R_p$ represents the Return of Portfolio (excluding risk-free rate for simplicity)

$$
R_{p,t} = \sum^n_{i=1}{w_{i,t-1}\cdot r_{i,t}}
$$
where $R_{p,t}$ is realized portfolio return over $n$ assets at time $t$

## Model Architecture
![[Screenshot 2023-06-27 at 21.50.54.png]]

## Input Layer



# Experiments

## Assets
- Use ETFs instead of individual assets
	- VIT, AGG, DBC, VIX
	- Problem becomes much easier & this trading strategy is more secure
	- Subsector indices not used because they're highly correlated