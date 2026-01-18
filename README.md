NIFTY – Regime-Based Quantitative Trading System
This project develops a regime-based quantitative trading system for the NIFTY 50 index using spot, futures, and options data. The system integrates market regime detection, technical indicators, options analytics, and machine learning to generate systematic and data-driven trading decisions while controlling risk across different market conditions.
Name: Muskan
Roll Number: 24/SCA/MCA/032

Project Overview
The objective of this project is to build an end-to-end quantitative trading framework that adapts to changing market behavior. Market regimes are identified using a Hidden Markov Model (HMM), and trading signals are generated using a 5/15 EMA crossover strategy filtered by detected regimes. Machine learning models are further applied to enhance trade selection and improve performance consistency.
Key Highlights

End-to-end quantitative trading system design

Multi-instrument analysis using spot, futures, and options

Market regime detection using Hidden Markov Models

Regime-filtered EMA trading strategy

Machine learning enhancement using XGBoost and LSTM

Statistical analysis of high-performance (outlier) trades

Professional, modular, and scalable project structure

Project Structure
nifty-regime-quant-system/
│
├── data/                # Raw and processed market data
├── notebooks/           # Step-by-step analysis notebooks
├── src/                 # Core Python modules
│   ├── data_utils.py
│   ├── features.py
│   ├── greeks.py
│   ├── regime.py
│   ├── strategy.py
│   ├── backtest.py
│   └── ml_models.py
│
├── models/              # Saved ML and HMM models
├── plots/               # Visualizations and charts
├── results/             # Backtest and analysis outputs
├── requirements.txt
└── README.md

Data Description & Instruments Used

Market: Indian Equity Index (NIFTY 50)

Frequency: 5-minute interval data

Duration: 1 year

Instruments:

NIFTY 50 Spot

OHLCV data

NIFTY Futures

Current month contract

OHLCV + Open Interest

Monthly contract rollover handling

NIFTY Options

ATM, ATM ±1, ATM ±2 strikes

Call and Put options

Implied Volatility, Open Interest, Volume

Market Regime Detection

Market regimes are identified using a Gaussian Hidden Markov Model (HMM) with three hidden states:

Uptrend (+1): Strong directional movement with favorable momentum

Downtrend (−1): Sustained bearish movement

Sideways (0): Low directional strength and range-bound behavior

Regime detection enables the strategy to trade only during favorable conditions, significantly reducing false signals and drawdowns during non-trending markets.

Outlier Trade Analysis

High-performance trades are identified using statistical outlier detection (Z-score > 3σ). These trades are analyzed to uncover patterns related to:

Market regime dominance

Time-of-day effects

Implied volatility behavior

Options Greeks exposure

EMA gap strength and trade duration

This analysis helps identify conditions that consistently produce exceptional returns and provides insights for further strategy refinement.
