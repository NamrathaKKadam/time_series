# Stock Price Prediction using LSTM

This project demonstrates how to use a **Long Short-Term Memory (LSTM)** neural network to predict stock prices based on historical data. It uses Apple's stock data fetched from Yahoo Finance and applies deep learning techniques to learn from past trends and forecast future prices.

---

## 📖 Project Overview

Time series forecasting is widely used in finance, economics, and business to predict future values based on past data. This project focuses on building an LSTM-based model that takes sequences of past closing prices and predicts the next day's price.

The project covers:
✔ Data fetching from Yahoo Finance  
✔ Preprocessing and normalization  
✔ Creating sequences for the LSTM model  
✔ Model building, training, and evaluation  
✔ Plotting and tabulating actual vs predicted prices

---

## 📂 Files

- `stocks_time_series.ipynb`: Jupyter Notebook implementing the LSTM model step-by-step.
- `README.md`: Project documentation and instructions.

---

## ✅ Steps Explained

### 1. **Import Libraries**
We use Python libraries like:
- `pandas`, `numpy` for data manipulation,
- `matplotlib` for plotting,
- `yfinance` for fetching stock data,
- `scikit-learn` for scaling,
- `tensorflow.keras` for building the LSTM model.

### 2. **Fetch Stock Data**
We download historical closing prices of Apple Inc. (`AAPL`) using `yfinance` from 2015 to 2025.

### 3. **Data Preprocessing**
Only the 'Close' price is selected, and it is normalized to the range [0, 1] to ensure better model convergence.

### 4. **Create Sequences**
We create sequences of past 60 days to predict the next day’s price. This helps the LSTM model learn temporal patterns.

### 5. **Split Data**
The data is split into training (80%) and testing (20%) datasets to train the model and evaluate its performance.

### 6. **Reshape Data**
LSTM expects input data in 3D form: (samples, time steps, features). We reshape the dataset accordingly.

### 7. **Build and Train the Model**
The LSTM model is built with 50 units and a Dense layer for output. The model is compiled using the Adam optimizer and Mean Squared Error (MSE) loss function, and trained over 50 epochs.

### 8. **Evaluate the Model**
The model's performance is evaluated by comparing predicted prices against actual prices using MSE, and results are plotted and tabulated.

---

## 📊 Results

The final output includes:
- A graph showing actual vs predicted stock prices.
- A table listing the actual and predicted closing prices along with corresponding dates.

---

## 📦 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/NamrathaKKadam/time_series.git
   cd time_series
