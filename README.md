# Binance Futures Testnet Trading Bot

## 📌 Overview

This is a Python-based CLI trading bot that interacts with Binance Futures Testnet (USDT-M).
It supports placing MARKET, LIMIT, and STOP-LIMIT orders with proper validation, logging, and error handling.

---

## ⚙️ Features

* Place MARKET, LIMIT, and STOP-LIMIT orders
* Supports BUY and SELL sides
* CLI-based input using argparse
* Input validation and error handling
* Logging of API requests and responses
* Clean modular structure

---

## 🛠️ Tech Stack

* Python 3.x
* python-binance
* argparse
* logging

---

## 📁 Project Structure

```
trading_bot/
│
├── bot/
│   ├── client.py
│   ├── orders.py
│   ├── validators.py
│   ├── logging_config.py
│
├── cli.py
├── requirements.txt
├── README.md
```

---

## 🔑 Setup Instructions

1. Clone the repository:

```
git clone https://github.com/your-username/binance-trading-bot.git
cd binance-trading-bot
```

2. Create virtual environment:

```
python -m venv venv
venv\Scripts\activate
```

3. Install dependencies:

```
pip install -r requirements.txt
```

4. Create `.env` file:

```
API_KEY=your_testnet_api_key
API_SECRET=your_testnet_api_secret
```

---

## ▶️ Usage Examples

### MARKET Order

```
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

### LIMIT Order

```
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --quantity 0.001 --price 71000
```

### STOP-LIMIT Order

```
python cli.py --symbol BTCUSDT --side BUY --type STOP_LIMIT --quantity 0.001 --price 71000 --stop_price 70000
```

---

## 📄 Logging

* Logs are stored in `bot.log`
* Includes:

  * API request details
  * API responses
  * Errors and exceptions

---

## ⚠️ Notes

* Testnet environment may not execute orders immediately
* LIMIT orders must follow market price rules
* API keys must be from Binance Testnet / Demo Trading

---

## ✅ Assignment Coverage

✔ MARKET order
✔ LIMIT order
✔ STOP-LIMIT order (Bonus)
✔ CLI input validation
✔ Logging and error handling
✔ Modular code structure

---
## sample output 1
📌 ORDER REQUEST
Symbol: BTCUSDT
Side: BUY
Type: MARKET
Quantity: 0.001
Price: None
Stop Price: None

✅ ORDER SUCCESS
Order ID: 13040244302
Status: NEW
Executed Qty: 0.0000
Avg Price: 0.00

##sample output 2
📌 ORDER REQUEST
Symbol: BTCUSDT
Side: SELL
Type: LIMIT
Quantity: 0.001
Price: 30000.0
Stop Price: None

❌ ORDER FAILED
Error: APIError(code=-4024): Limit price can't be lower than 70583.39.

##sample output 3

📌 ORDER REQUEST
Symbol: BTCUSDT
Side: SELL
Type: LIMIT
Quantity: 0.001
Price: 71000.0
Stop Price: None

✅ ORDER SUCCESS
Order ID: 13040256947
Status: NEW
Executed Qty: 0.0000
Avg Price: 0.00

## 👨‍💻 Author

Manoj Kumar Naraboina
