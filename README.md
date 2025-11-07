# 📊 Extracting and Visualizing Stock Data

This project demonstrates how to extract stock market data using Python, process it using popular data science libraries, and visualize trends to support data-driven insights.

---

## 🧠 Project Overview

Stock data analysis is a critical part of data science and finance.  
In this project, you’ll learn how to:
- Retrieve stock price data using **Yahoo Finance (yfinance)**.
- Perform **data cleaning and manipulation** with Pandas.
- **Visualize** stock trends over time.
- Optionally, extract additional company information from the web using **BeautifulSoup**.

---

## ⚙️ Installation & Requirements

Before running the notebook, install the required Python libraries:

```bash
pip install yfinance pandas requests beautifulsoup4 plotly matplotlib
```

---

## 📦 Libraries Used

| Library | Purpose |
|----------|----------|
| `pandas` | Data manipulation and analysis |
| `yfinance` | Fetching stock market data |
| `numpy` | Numerical computations |
| `requests` | Fetching web data |
| `beautifulsoup4` | Web scraping (for company information) |
| `matplotlib` / `plotly` | Data visualization |

---

## 📈 Features Implemented

### 1. Extract Tesla Stock Data  
Using the **yfinance** API:
```python
import yfinance as yf
tesla = yf.Ticker("TSLA")
tesla_data = tesla.history(period="max")
tesla_data.reset_index(inplace=True)
```

### 2. Analyze Historical Trends  
The dataset includes:
- Date  
- Open, High, Low, Close Prices  
- Volume  
- Dividends and Stock Splits  

You can compute moving averages or daily returns for deeper analysis.

### 3. Visualize Data  
Plot closing price trends:
```python
import matplotlib.pyplot as plt

plt.figure(figsize=(10,5))
plt.plot(tesla_data['Date'], tesla_data['Close'])
plt.title('Tesla Stock Closing Prices Over Time')
plt.xlabel('Date')
plt.ylabel('Closing Price (USD)')
plt.show()
```

---

## 🧩 Optional Extension Ideas
You can expand the project by:
- Comparing multiple companies (e.g., Tesla vs. Ford vs. GM)
- Adding interactive visualizations with Plotly
- Building a Streamlit dashboard
- Performing time-series forecasting using ARIMA or LSTM

---

## 🧑‍💻 Author
**Tushar** — 4th-year Computer Science Engineering Student  
Focus Areas: AI, ML, Data Science, Python Development
 **Note:** - It's and coursera  capstone project   

---


