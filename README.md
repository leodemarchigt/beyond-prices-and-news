# 📈 Beyond Prices and News

> **A deep learning framework for stock market forecasting using market data, financial news and macroeconomic indicators.**

This repository contains the implementation and the paper of a university project developed at the **University of Padua**.

---

## Overview

Financial markets are influenced by many interconnected factors beyond historical prices. This project investigates whether combining **technical indicators**, **macroeconomic variables**, and **financial news sentiment** can improve forecasting performance over traditional deep learning approaches.

The proposed framework employs an **ensemble learning architecture** that blends the predictions of two recurrent neural networks (LSTM and GRU) through a fully connected meta-learner.

---

## Architecture

```text
Market Prices  ───────────────┐
                              │
Financial News ──► FinBERT ───┼──► Feature Engineering
                              │
Macroeconomic Indicators ─────┘
               │
               ▼
      Rolling Time Windows
               │
     ┌─────────┴─────────┐
     │                   │
    LSTM               GRU
     │                   │
     └─────────┬─────────┘
               ▼
      Meta-Learner (MLP)
               │
               ▼
        Market Forecast
```

---

## Features

* 📊 S&P 500 historical prices
* 📰 Financial news sentiment extracted with **FinBERT**
* 📉 Technical indicators (RSI, Moving Averages, Rolling Volatility)
* 🌍 Macroeconomic indicators (VIX, Treasury Yield Spread, WTI Oil)
* 🤖 LSTM + GRU ensemble learning
* ⚙️ Hyperparameter optimization with Optuna

---

## Results

Compared with standalone recurrent models, the proposed framework achieved:

| Metric               |                                             Improvement |
| -------------------- | ------------------------------------------------------: |
| Mean Squared Error   |                                     **up to 33% lower** |
| F1-score             |                                     **over 40% higher** |
| Directional Accuracy | **≈26% higher** than the original two-feature framework |

The experiments show that integrating heterogeneous financial signals produces more robust predictions than relying on prices and news sentiment alone.

---

## Repository

```text
.
├── notebook.ipynb              # Complete implementation
├── Beyond_Prices_and_News.pdf  # Project report
├── README.md
```

---

## Dataset

The datasets are **not included** because of their size.

Data were collected from:

* Yahoo Finance
* FRED (Federal Reserve Economic Data)
* FNSPID Financial News Dataset

---

## Paper

The complete methodology, experiments and discussion are available in:

📄 **Beyond_Prices_and_News.pdf**

---

## Technologies

* Python
* PyTorch
* pandas
* NumPy
* scikit-learn
* Optuna
* FinBERT
* yfinance
* matplotlib

---

## Future Improvements

* Transformer-based forecasting models
* Continual learning
* Additional market indicators
* Volatility-aware loss functions
* Larger and more diverse datasets

---

## Author

**Leonardo De Marchi**

M.Sc. in Control Systems Engineering
University of Padua

