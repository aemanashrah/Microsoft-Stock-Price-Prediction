📈 Microsoft Stock Price Forecasting (MSFT) using Deep Learning
🚀 Project Overview
This project builds a robust Time-Series forecasting model to predict Microsoft's (MSFT) future stock prices. Moving beyond basic linear predictions, this project engineers complex technical market indicators and leverages a Long Short-Term Memory (LSTM) neural network to capture the sequential memory and volatility of the stock market.
The final model successfully tracks historical pricing trends and generates a dynamic, 30-day future market forecast that simulates natural market variance.
🧠 Technical Stack
Language: Python
Deep Learning: TensorFlow / Keras (LSTM)
Machine Learning & Preprocessing: Scikit-Learn (MinMaxScaler, RMSE, MAE, R2)
Data Manipulation: Pandas, NumPy
Visualization: Matplotlib, Seaborn
Data Sourcing: yfinance API / Historical CSV Data
⚙️ Pipeline & Key Features
1. Advanced Feature Engineering:
Calculates and integrates key technical indicators used by real-world traders to give the neural network context regarding momentum and volatility:
SMA & EMA (20-Day Simple & Exponential Moving Averages)
Bollinger Bands (2 Standard Deviations)
RSI (14-Day Relative Strength Index)
2. Data Preprocessing for Time-Series:
Cleaned and interpolated missing values smoothly over time.
Scaled all features between 0 and 1 using MinMaxScaler (fit strictly to training data to prevent future-data leakage).
Converted tabular data into 60-day 3D sequential windows ([Samples, Time Steps, Features]) optimized for Deep Learning.
3. Model Benchmarking & Architecture:
Benchmarked traditional models (Linear Regression, Random Forest, XGBoost).
Selected a Deep Learning LSTM Architecture for its superior ability to handle long-term dependencies.
Designed with stacked LSTM layers and Dropout(0.2) regularization to prevent overfitting.
4. Dynamic 30-Day Forecasting:
Solved the "Vanilla LSTM Flatline" problem by dynamically recalculating moving averages, Bollinger bands, and RSI on every future loop step.
Injected historical High/Low ratio structures and mathematical standard deviations (random walk) to simulate realistic market variance for the predicted curve.
📊 Results
The LSTM model demonstrates a high $R^2$ accuracy score on the hidden test set, successfully predicting sudden drops and rallies in the market. The final output generates a seamless Matplotlib visualization combining historical data, test-set tracking accuracy, and a realistic 30-day future projection curve.

<img width="827" height="447" alt="Screenshot 2026-06-18 174218" src="https://github.com/user-attachments/assets/777bbd0f-b555-4856-a995-6dfe6e16a474" />
