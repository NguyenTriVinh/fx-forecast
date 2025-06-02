# FX Forecast

**FX Forecast** is a research-oriented project aimed at predicting foreign exchange (Forex) rates between the US Dollar (USD) and major global currencies including the Australian Dollar (AUD), Euro (EUR), British Pound (GBP), and Japanese Yen (JPY). This project implements a variety of machine learning and deep learning models to analyze time-series data and generate robust currency forecasts.

The purpose of this project is to explore the effectiveness of different forecasting techniques, from statistical models to advanced neural networks, in modeling and predicting Forex trends.

---

## Motivation

The Forex market is the largest and most liquid financial market in the world, where trillions of dollars are exchanged daily. Accurate prediction of currency exchange rates has numerous applications, including algorithmic trading, macroeconomic policy formulation, and risk management.

Due to the stochastic nature of currency fluctuations and the presence of external influencing factors (news, interest rates, inflation, etc.), forecasting exchange rates is a challenging yet impactful problem in data science and finance.

---


## 🤖 Models Implemented

We evaluate several modeling strategies from statistical baselines to deep neural networks:

| **Model**     | **Description**                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------|
| **ARIMAX**     | Autoregressive Integrated Moving Average with Exogenous Variables — suitable for time series with external factors. |
| **LSTM**       | Long Short-Term Memory — a recurrent neural network effective for sequential time series modeling. |
| **GRU**        | Gated Recurrent Unit — a lightweight variant of LSTM with comparable performance.               |
| **Transformer**| Attention-based model architecture ideal for learning long-term dependencies.                   |
| **LightGBM**   | Gradient boosting framework with high speed and accuracy on tabular data.                       |

Each model is tested independently on all four currency pairs to evaluate generalization ability across different economic regions.

---

## 🔄 Data Pipeline

1. **Raw CSVs** in `Dataset/` contain historical exchange rates from investing.com.
2. **Preprocessing scripts** located in `Train-Test Split Dataset/` generate clean and normalized datasets.
3. **Training & evaluation** are handled by each model-specific directory.
4. **Results** (graphs, metrics) are generated and logged per notebook/script.

The time series are split into training and testing sets using a fixed ratio and processed into supervised learning format (e.g., sliding windows, lag features, etc.).

---

## 📊 Evaluation Metrics

We assess the performance of each forecasting model using the following metrics:

- **MSE** (Mean Squared Error)
- **MAE** (Mean Absolute Error)
- **RMSE** (Root Mean Squared Error)
- **R² Score** (Coefficient of Determination)

These metrics allow for both error quantification and performance comparison between models.

---

## 📦 Dependencies

Core technologies used:

- Python 3.x
- NumPy, Pandas
- Scikit-learn
- Statsmodels
- TensorFlow / Keras
- LightGBM
- Matplotlib / Seaborn