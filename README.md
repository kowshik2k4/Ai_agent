# 💬 AI Agent for Stock Market Prediction
This AI agent leverages historical stock market data fetched via the yfinance library to perform accurate and insightful stock price forecasting. Utilizing fbprophet — a powerful time series forecasting tool developed by Facebook — the agent models trends, seasonality, and market cycles to predict future stock prices with high precision.

[![Open in Streamlit]Coming soon

### How to run it on your own machine
Script will run by itself on any code editor

# 🚀 Features
1. Fetches real-time stock data using Yahoo Finance API (yfinance)
   * Historical data from Jan 2015 to the present

2. AI-powered prediction
    * Uses fbprophet to forecast future prices for the next 4 years
    * Interactive visualizations
    * Displays actual vs. predicted prices on dynamic charts

3. User-friendly UI
    * Built with Streamlit for seamless user interaction

# 🛠️ Tech Stack & Architecture
## 🧰 Libraries Used
|Library	  |Purpose|
| ---  | ---  |
|streamlit|	      UI development and state management|
|yahooquery	|              	Fetching historical stock market data|
|dateandtime,pytz| Provides classes for manipulating dates and times ( |
|click| package for creating command-line interfaces (CLIs);|
|prophet| 	Time series forecasting |
|pandas| 	Data preprocessing and manipulation|
|matplotlib, plotly| 	Graphical data visualization|

# App Flow
* On launch, Stockify prompts the user to input a stock ticker (e.g., AAPL, GOOGL).
* Historical stock data from 2015 onward is fetched using the yfinance API.
* The data is preprocessed and passed to Facebook Prophet, which models trends and seasonality.
* A forecast is generated for the next 4 years and displayed alongside past trends.
* Users can interact with plots to explore patterns and predictions.



# 🔐 Requirements
* Python 3.8+
* Internet connection (for Yahoo Finance API access)
* No authentication needed unless deploying with access limits

# 💡 Challenges & Solutions
* Challenge: Long-term prediction on noisy financial data
   * ✅ Solution: Used robust trend detection via Prophet and excluded low-variance data when necessary.
     
* Challenge: Handling missing or incomplete data
  * ✅ Solution: Implemented preprocessing to clean and fill time-series gaps.

* Challenge: UI responsiveness and live updates
   * ✅ Solution: Used st.cache_data() and session state tracking in Streamlit to reduce reload delays.
  
