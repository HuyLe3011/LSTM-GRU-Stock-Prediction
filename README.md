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
While the model demonstrates strong out-of-sample performance, it was developed under academic constraints. Future iterations will address the following real-world market dynamics:

* **Survivorship Bias:** The current dataset consists of the top 50 highly liquid HOSE stocks over the 2018–2023 period. Future work will utilize Point-in-Time (PiT) data, including delisted entities, to prevent the inflation of risk-adjusted returns.
* **Market Friction & Slippage:** The backtest assumes standard transaction costs but does not fully account for market impact during high-turnover rebalancing. I plan to integrate a Transaction Cost Penalty directly into the Deep Learning loss function.
* **Regime Shift Overfitting:** To prevent model decay during macroeconomic shifts, future pipelines will replace the static train/test split with Walk-Forward Validation and Hidden Markov Models (HMM) for dynamic regime detection.
