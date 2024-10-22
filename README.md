# Portfolio Optimization with FastAPI and Python

This project implements a **Portfolio Optimization** algorithm that helps allocate an investment budget across a set of stocks in an optimal way. The objective is to maximize the **Sharpe Ratio**, which is a measure of risk-adjusted return, while working within a given budget (e.g., $1000).

## Project Overview

The portfolio optimization is based on **Modern Portfolio Theory (MPT)** and uses historical stock price data to allocate a given budget across selected stocks. The aim is to maximize the expected return while minimizing risk, considering constraints such as the initial budget, avoiding short selling, and discrete allocation (whole stocks).

The key components of the project include:
- **Efficient Frontier**: A visual representation of the best risk-return combinations.
- **Sharpe Ratio Maximization**: Aiming for the highest risk-adjusted returns.
- **FastAPI Integration**: A REST API to run the optimization and get results.
- **Discrete Allocation**: Allocating whole stocks, respecting the initial budget.

## Features

- **Maximization of the Sharpe Ratio** to find the optimal risk-adjusted return.
- **Efficient Frontier Plotting**, showing various risk-return trade-offs and the maximum Sharpe Ratio portfolio.
- **Stock Selection** based on historical returns and volatility.
- **Discrete Stock Allocation**, ensuring no fractional shares are purchased while staying within the budget.
- **FastAPI Backend** to serve the portfolio optimization as an API.

## Assumptions

The portfolio optimization operates under several key assumptions:
1. **Historical Data**: We use the last 5 years of stock price data to estimate future performance, assuming that historical returns are indicative of future returns.
2. **Sharpe Ratio**: The optimization focuses on maximizing the Sharpe Ratio, which assumes investors prefer higher returns for less risk.
3. **Top 10 Tickers**: Only the top 10 stocks with above-average returns are considered in the optimization.
4. **Budget Constraint**: The total investment is capped at $1000.
5. **No Short Selling**: Only long positions are considered, meaning no borrowing of stocks for sale.

These assumptions simplify the problem, making it easier to achieve actionable insights for an investor.

## Installation

To run this project, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/Portfolio-Optimization.git
   cd Portfolio-Optimization
