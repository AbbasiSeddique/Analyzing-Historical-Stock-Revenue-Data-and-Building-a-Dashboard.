# Analyzing-Historical-Stock-Revenue-Data-and-Building-a-Dashboard.
This project analyzes historical **stock price data** and **company revenue data**, visualizes them in interactive dashboards, and applies a **machine learning model** to generate predictive buy signals based on technical indicators.

It combines:

* Financial data retrieval
* Web scraping
* Interactive visualization
* Machine learning backtesting

---

## 🚀 Project Features

* 📊 **Stock Price Analysis** using Yahoo Finance (`yfinance`)
* 🌐 **Revenue Data Scraping** using `BeautifulSoup`
* 📉 **Interactive Dashboards** with Plotly
* 🤖 **Machine Learning Predictions** using Random Forest
* 🔁 **Backtesting Framework** to evaluate prediction performance
* 📋 **Precision-based Evaluation** for trading signals

---

## 🧠 Technologies Used

* Python
* yfinance
* pandas
* requests
* BeautifulSoup
* plotly
* scikit-learn

---

## 📂 Project Workflow

### 1️⃣ Stock Data Collection

Stock price data is fetched from Yahoo Finance for multiple tickers:

```
AAPL, NVDA, META, GME, TSLA
```

Data includes:

* Open
* High
* Low
* Close
* Volume

---

### 2️⃣ Revenue Data Scraping

Revenue data is scraped from financial tables hosted online using:

* `requests`
* `BeautifulSoup`
* `pandas.read_html`

Cleaned revenue data includes:

* Date
* Revenue (USD, millions)

---

### 3️⃣ Interactive Dashboard

An interactive Plotly dashboard is generated showing:

* 📈 Stock Price (Line Chart)
* 💰 Revenue (Bar Chart)
* Dual Y-Axis for clear comparison

Dashboards are created for:

* Tesla
* GameStop

---

### 4️⃣ Feature Engineering

Custom technical indicators are generated using rolling windows:

* Close Price Ratios
* Trend-based indicators
* Multiple horizons: `2, 5, 60, 250, 1000` days

These features help capture short-term and long-term market behavior.

---

### 5️⃣ Machine Learning Model

A **Random Forest Classifier** is trained to predict whether the stock price will go up the next day.

* Target variable:

  ```
  Tomorrow Close > Today Close
  ```
* Probability threshold: **0.60**
* Model:

  ```
  RandomForestClassifier(
      n_estimators=200,
      min_samples_split=50
  )
  ```

---

### 6️⃣ Backtesting Strategy

A rolling-window backtesting approach is used to simulate real trading conditions:

* Train on historical data
* Test on unseen future data
* Evaluate predictions over time

---

## 📊 Final Results

| Ticker | Precision Score | Buy Signals Sent |
| ------ | --------------- | ---------------- |
| AAPL   | 52.51%          | 577              |
| NVDA   | 58.14%          | 301              |
| META   | 54.93%          | 142              |
| GME    | 49.38%          | 401              |
| TSLA   | 50.00%          | 70               |

**Precision Score** indicates how often predicted buy signals were correct.

---

## ⚠️ Disclaimer

This project is for **educational and research purposes only**.
It is **not financial advice** and should not be used directly for live trading.

---

## 🧩 Future Improvements

* Add more technical indicators (RSI, MACD, Bollinger Bands)
* Include transaction cost modeling
* Improve feature selection
* Add deep learning models
* Deploy dashboards via Streamlit or Dash

---

## 👤 Author

**Seddique Abbasi**
Data Science | Machine Learning | Financial Analysis

