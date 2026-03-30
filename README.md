# Gold Price Prediction with Machine Learning

An end-to-end Machine Learning pipeline designed to forecast the next-day closing price of Gold, aiming to enhance quantitative trading strategies.

This project explores and compares deep learning approaches versus tree-based ensemble models to capture complex, non-linear market patterns.

## Models Implemented

* **Random Forest Regressor (RF):** Utilized for its robust handling of non-linear relationships in financial markets.
* **Gradient Boosting Regressor (GBR):** Configured to optimize predictions by focusing on sequential error reduction.
* **Long Short-Term Memory (LSTM):** A recurrent neural network architecture designed to capture sequential and temporal dependencies in price action[cite: 43].

## Feature Engineering

The models were trained on a comprehensive set of technical indicators and historical data[cite: 18]:

* **Price Action & Volume:** Close, High, Low, Open, Volume[cite: 27].
* **Scaled Metrics:** Scaled Return, Scaled Volatility, Scaled Volume[cite: 20, 21, 22].
* **Technical Indicators:** Moving Averages (EMAs), Bollinger Bands, ADX[cite: 23, 24, 25].
* **Temporal Lags:** 20-period lookback to incorporate historical dependencies[cite: 26].

## Key Findings & Performance

The **Random Forest** model demonstrated the strongest short-term performance[cite: 204]:

* **Accuracy:** Achieved an $R^{2}$ of 0.9781 and a Mean Absolute Error (MAE) of 31.65[cite: 63, 64].
* **Trading Viability:** Simulated backtesting yielded a **27.83% return** with a 62% win rate on positive trades[cite: 65, 204].

While the LSTM captured baseline temporal patterns, it requires further tuning (e.g., expanded 60-90 day windows and integration of macroeconomic variables) to outperform the tree-based models in this specific timeframe[cite: 208, 209].

## Repository Structure

* `notebooks/`: Contains the Jupyter Notebook (`.ipynb`) with the full Python code, data preprocessing, and model evaluation.
* `docs/`: Contains the full academic research paper (PDF) detailing the methodology and statistical analysis.
