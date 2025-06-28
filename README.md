#  Algo Trading Automation System

This project is a **algorithmic trading system** that is ML-augmented and rule-based, and it does the following:


Pulls daily stock data from Yahoo Finance and uses moving averages and RSI to implement a strategy.
Logs buy signals to Google Sheets
It incorporates a basic machine learning model (Decision Tree & Logistic Regression) and sends Telegram alerts for trades and ML predictions.
Completely automated and modular

---

## Features

The feature is described as follows: 

  Strategy Logic | RSI < 30 and 20-DMA > 50-DMA = BUY signal | |  Backtest | 6-month historical backtest on NIFTY 50 stocks | |  ML Model (Bonus) | Predicts next-day price direction using RSI, MACD, MA20, MA50, Volume | |  Google Sheets Logging | All trades and performance summary auto-logged | |  Telegram Alerts | Alerts for trade signals & ML prediction | |  Modular Code | Clean steps for Data Ingestion, Indicators, Strategy, Logging, ML, Alerts |

##  Steps Dissection

Inside the notebook, each module is organized step-by-step.

| Step | Description | |------|-----------------------------------|| 1 | Install dependencies + import modules || 2 | Define TICKERS and fetch data || 4 | Add indicators (RSI, MACD, MA20, MA50)|| 8-10 | Log trades + performance summary || 11 | Plot MA and signals for all stocks || 12 | Simulate profit & P&L || 13 | ML prediction (Decision Tree & Linear Regression) || 14 | Send Telegram alert for predictions |

---

## Google Sheets Output

### Trade Log![Trade Log](sheets_output/sheets_trade_log.png)

### Overview Sheet![Recap](sheets_summary.png/sheets_output)

### ML Prediction [ML Forecast](sheets_output/sheets_ml_prediction.png)

---

## 🔧 Tech Stack

**Python 3** - `yfinance`, `ta`, `pandas`, `gspread`, `sklearn`
- Google Sheets API (through `creds.json`)
Google Colab and the Telegram Bot API (Suggested)

---

## Telegram Alerts 

**Bot:** `@TradeAI_Notifier_bot` - **Trigger:** ML prediction or buy signal - Alert format: