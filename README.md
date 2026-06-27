# Beyond Prices and News

A deep learning framework for stock market forecasting that combines financial time series, macroeconomic indicators and news sentiment through an ensemble learning architecture.

This repository contains the implementation and the paper developed as part of a university project at the **University of Padua**.

---

## Project Overview

The objective of this project is to improve stock market forecasting by integrating multiple sources of information instead of relying only on historical prices.

The proposed framework combines:

* Historical S&P 500 price data
* Financial news sentiment (FinBERT)
* Macroeconomic indicators (VIX, Treasury Yield Spread, WTI Oil)
* Technical indicators (RSI, moving averages, rolling volatility)

Two recurrent neural networks (LSTM and GRU) are trained independently and their predictions are combined through a feed-forward meta-learner using a blending ensemble strategy.

---

## Repository Structure

```
.
├── notebook.ipynb          # Main implementation
├── Beyond_Prices_and_News.pdf
├── requirements.txt
├── README.md
└── data/                   # Dataset (not included)
```

---

## Main Features

* Financial time-series forecasting
* Feature engineering on market data
* Financial sentiment analysis with FinBERT
* LSTM + GRU ensemble
* Hyperparameter optimization with Optuna
* Evaluation using both regression and directional metrics

---

## Results

Compared to standard LSTM and GRU baselines, the proposed framework achieves:

* up to **33% lower Mean Squared Error (MSE)**
* over **40% improvement in F1-score**
* approximately **26% higher Mean Directional Accuracy** compared to the original two-feature framework

These results highlight the benefits of combining heterogeneous financial signals into a single forecasting model.

---

## Dataset

The datasets used in this project are **not included** in the repository due to their size.

Data sources include:

* Yahoo Finance (S&P 500)
* FRED (Federal Reserve Economic Data)
* FNSPID financial news dataset

After downloading the data, place them inside the `data/` directory.

---

## Paper

The complete methodology, experiments and discussion are available in:

**Beyond_Prices_and_News.pdf**

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

---

## Author

Leonardo De Marchi
MSc in Control Systems Engineering
University of Padua
