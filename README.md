# ETH Trading Strategy using Regime Detection + GARCH Modeling

## Overview
This project builds a **regime-aware trading strategy for Ethereum (ETH)** by combining time series modeling, volatility estimation, and probabilistic regime detection.

The goal is to move beyond static forecasting and enable **adaptive decision-making based on market conditions**.

---

## Problem Statement
Cryptocurrency markets exhibit:
- High volatility
- Regime shifts (bull, bear, crisis)
- Non-stationary behavior

Traditional models fail to adapt to these dynamics.

This project answers:
**Can we dynamically adjust trading decisions using regime-aware forecasting?**

---

## Approach

### 1. Data Collection
- ETH-USD historical price data (via yfinance)

### 2. Feature Engineering
- Log returns
- Rolling volatility
- Volatility clustering indicators

### 3. Regime Detection
- Markov Regime Switching Model
- Identifies multiple market states:
  - Low volatility (stable)
  - Medium volatility
  - High volatility (crisis)

### 4. Volatility Modeling
- GJR-GARCH model to capture:
  - Volatility clustering
  - Asymmetric shocks

### 5. Forecasting & Strategy
- Combine:
  - Expected returns (AR component)
  - Regime probabilities
  - Forecasted volatility

- Generate:
  - Expected 30-day returns
  - Dynamic position sizing
  - Risk-adjusted exposure

---

## Key Highlights
- Regime-aware forecasting vs static models  
- Combines statistical modeling + financial intuition  
- Walk-forward validation for realistic performance  
- Dynamic risk management using volatility scaling  

---

## Results (Illustrative)
- Improved risk-adjusted returns vs naive strategies  
- Better drawdown control during high-volatility regimes  
- Adaptive exposure based on market conditions  

---

## Tech Stack
- Python  
- pandas, numpy  
- statsmodels (Markov Regression)  
- arch (GARCH models)  
- matplotlib / plotly  

---

## Repository Structure
├── eth_trading_strategy_regime_model.ipynb
├── ETH_Model_Building_Trading_Strategy.html
├── README.md

## Key Concepts Used
- Time Series Analysis  
- Regime Switching Models  
- GARCH / Volatility Modeling  
- Walk-Forward Backtesting  
- Risk-Based Position Sizing  

---

## Business / Product Perspective
This project demonstrates how advanced modeling can be translated into:
- Actionable trading strategies
- Risk-aware decision systems
- Adaptive AI-driven financial products

---

## Future Improvements
- Incorporate macro signals (rates, inflation, BTC correlation)  
- Use ML models (XGBoost, LSTM) for return prediction  
- Add transaction costs & slippage modeling  
- Deploy as a real-time trading system  

---
