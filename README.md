# Price-Movement-Classification

# 📈 Price Movement Classification using Technical Indicators

This project aims to predict whether a stock's price will go **up** or **not up** the next day using past returns and technical indicators like RSI, MACD, and moving averages.

---

## 🧠 Problem Statement

Build a binary classification model that can predict:
- **1** → if the next day's stock price increases  
- **0** → if it stays the same or decreases

---

## 📊 Data

- Source: [Yahoo Finance](https://finance.yahoo.com/)
- Ticker used: `NVDA` (NVIDIA Corporation)
- Time period: Jan 1, 2020 to Dec 31, 2020
- Downloaded using the `yfinance` Python library

---

## 🔨 Features Used

The following features (technical indicators) were computed:

| Feature        | Description |
|----------------|-------------|
| `returns`      | Daily percent change in closing price |
| `RSI`          | Relative Strength Index (momentum indicator) |
| `MACD`         | Moving Average Convergence Divergence |
| `MA_10`        | 10-day moving average of close prices |

---

## 🎯 Label Definition

```python
target = 1 if next_day_close > today_close else 0
