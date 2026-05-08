# Multi-Asset Financial Performance & Strategy Analysis

## 📊 Project Overview
This project provides a comprehensive quantitative analysis of four major financial instruments: **NSE Index (Nifty 50)**, **NSE Bank Index**, **Gold**, and **Silver**. By integrating historical data analysis with time-series forecasting and algorithmic backtesting, this study evaluates asset correlations, risk-adjusted returns, and the effectiveness of trend-following strategies.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `Pandas` & `NumPy` (Data Wrangling)
    * `Matplotlib` & `Seaborn` (Advanced Visualization)
    * `Statsmodels` (Holt-Winters Time-Series Forecasting)

## 📂 Project Structure
* `Financial_analysis_project.ipynb`: Main Jupyter Notebook containing all analysis and visuals.
* `NSEI_data.csv` / `NSEBANK_data.csv`: Equity index historical data.
* `GOLDBEES.NS_data.csv` / `SILVERBEES.NS_data.csv`: Commodity ETF historical data.
* `README.md`: Project documentation.

## 🚀 Key Analysis Phases

### 1. Data Engineering & Standardization
* Consolidated disparate CSV datasets into a unified "Long Format" DataFrame.
* Implemented **automated path handling** using `os.path.join` and `os.getcwd()` to ensure project portability across different operating systems.
* Engineered technical features including **20-day and 50-day Simple Moving Averages (SMA)**.

### 2. Exploratory Data Analysis (EDA)
Comprehensive visualization of market dynamics, including:
* **Price Trends:** Comparative analysis of all four assets with SMA overlays.
* **Volatility Analysis:** Daily return distributions and standard deviation comparisons.
* **Return Distributions:** Monthly and daily return histograms and box plots to identify market outliers.
* **Logarithmic Scaling:** Monthly price trends on a log scale for better long-term growth visualization.

### 3. Quantitative Insights (Portfolio Logic)
* **Correlation Matrix:** Analyzed the relationship between equities and commodities to determine diversification benefits.
* **Sharpe Ratio Calculation:** Determined the risk-adjusted performance (Annualized) to identify the most efficient asset.
* **MA Crossover Backtest:** Simulated a 20/50 day SMA crossover strategy against a "Buy & Hold" benchmark for the NSE Index.

### 4. Predictive Modeling
* Applied **Holt-Winters Exponential Smoothing** to the NSE Index.
* Accounted for **Trend** and **Seasonality** to forecast market movement for the upcoming 12-month period.

## 📈 Key Findings
* **Diversification:** Identified low correlation between Gold/Silver and Equity Indices, suggesting strong hedging potential.
* **Risk-Efficiency:** The Sharpe Ratio analysis highlights which assets provided the best return per unit of volatility.
* **Forecast Accuracy:** The Holt-Winters model successfully captured the upward momentum while adjusting for seasonal variations in the Indian markets.

## 🔧 How to Run
1. Clone this repository.
2. Ensure all `.csv` files are in the same folder as the `.ipynb` notebook.
3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn statsmodels
