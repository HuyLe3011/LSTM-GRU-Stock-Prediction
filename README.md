# 📈 Hybrid LSTM-GRU Model for Stock Price Prediction

## 📌 Project Overview
This repository contains the source code and datasets for my Graduation Thesis. The project proposes a hybrid Deep Learning approach, combining **Long Short-Term Memory (LSTM)** and **Gated Recurrent Unit (GRU)** networks, to predict the future price movements of the VNINDEX and major blue-chip stocks (FPT, HPG, VCB) in the Vietnamese equity market.

## 🗂️ Project Structure
* `data/`: Contains historical OHLCV data for VNINDEX, FPT, HPG, and VCB (fetched using `vnstock`).
* `notebooks/`: Jupyter notebooks demonstrating the Exploratory Data Analysis (EDA), data preprocessing, model architecture, training process, and evaluation for each ticker.

## 🚀 Key Technologies
* **Deep Learning:** TensorFlow / Keras (LSTM, GRU)
* **Data Processing:** Pandas, NumPy, Scikit-learn (MinMaxScaler)
* **Financial Data API:** `vnstock`

## ⚙️ How to Run
1. Clone this repository:
```bash
git clone [https://github.com/HuyLe3011/LSTM-GRU-Stock-Prediction.git](https://github.com/HuyLe3011/LSTM-GRU-Stock-Prediction.git)
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

3. Open the `notebooks/` directory and run the specific `.ipynb` file for the desired ticker.

## ⚠️ Known Limitations & Future Work
The hybrid LSTM-GRU architecture successfully models historical patterns, but continuous improvement requires addressing the following areas:

* **Time-Series Lag Effect:** Deep learning models predicting absolute price levels often suffer from a one-step lag during trend reversals. Future iterations will shift the target variable from absolute prices to stationary returns or volatility forecasting.
* **Exogenous Variables:** The current model is predominantly autoregressive, relying purely on OHLCV data. I plan to integrate macroeconomic factors (e.g., interest rates, exchange rates) and sentiment analysis to improve predictive accuracy during sudden market shocks.
* **Hyperparameter Optimization:** Future work will implement systematic hyperparameter tuning frameworks (e.g., Optuna or Bayesian Optimization) to dynamically search for the optimal network architecture across different assets.
