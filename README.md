# Nifty 50 Next-Day Close Prediction

Hybrid LSTM-Transformer that predicts the next-day Nifty 50 close, with a 90% interval from Monte Carlo dropout and a BUY/SELL/HOLD signal, served in a Streamlit app.

## Overview
- Data: Nifty 50 daily OHLCV (Kaggle + Yahoo Finance), 1990–2026
- Features: 15 technical indicators, rolling 252-day z-score, 60-day windows
- Model: 2-layer LSTM (128) + 2-layer Transformer (4 heads) + dense head
- Target: next-day log return, converted to an exact price
- Uncertainty: 100 MC-dropout passes, calibrated on validation data
