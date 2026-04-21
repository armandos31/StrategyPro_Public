# StrategyPro

**StrategyPro** is an open-source trading system analysis platform built with [Streamlit](https://streamlit.io/). It lets you import trade exports, organize your strategies, and analyze individual systems or entire portfolios with interactive charts, correlation matrices, and performance metrics.

---

## Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/armandoloconte/StrategyPro_Public.git
cd StrategyPro_Public

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the app
streamlit run main.py
```

---

## Importing Trades

Export your trades from your trading platform as a **comma-separated file** with the following columns **in this exact order**:

| Column | Format | Description |
|---|---|---|
| `EntryDate-Time` | `MM/DD/YYYY HH:mm:ss` | Trade entry timestamp |
| `EntryPrice` | numeric | Strategy entry price |
| `ExitDate-Time` | `MM/DD/YYYY HH:mm:ss` | Trade exit timestamp |
| `ExitPrice` | numeric | Strategy exit price |
| `SymbolName` | string | Traded instrument name |
| `MarketPosition` | `1` / `-1` | `1` = Long, `-1` = Short |
| `MaxContracts` | numeric | Number of contracts/shares traded |
| `Profit/Loss` | numeric | Net profit or loss of the trade |
| `MaxPositionProfit` | numeric | Maximum unrealized profit during the trade |
| `MaxPositionLoss` | numeric | Maximum unrealized loss during the trade |

All values must be on a **single line per trade**, separated by commas, with no header row.

![Import result](https://github.com/user-attachments/assets/1a7bec39-d248-44fb-9c8c-54d7c9dd9968)

---

## Features

### Report Manager
Upload and organize your strategy reports. The tool automatically saves them and lets you attach custom tags for easy filtering across all other sections. If you replace an existing report with an updated version, your tags are preserved.

<img width="705" alt="Report Manager" src="https://github.com/user-attachments/assets/7099bbe6-45f2-4d18-acc0-6e9585425914">

---

### Symbol Manager
Register the symbols traded by your strategies, along with margin requirements and target markets. Symbol metadata is used throughout the platform to enable more granular analysis and filtering.

<img width="402" alt="Symbol Manager" src="https://github.com/user-attachments/assets/477987d7-4aca-4074-a057-b79e9cc56db5">

---

### Comparator
Quickly rank and compare large numbers of strategies across markets and time periods. Filter by market (e.g. Nasdaq, Forex, Equities), tags, or date range, and instantly identify the best-performing systems using an interactive table and charts.

> *100 strategies on Nasdaq, 50 on soybeans, 400 on Forex — find the top performer in the last 2 months in seconds.*

<img width="1040" alt="Comparator" src="https://github.com/user-attachments/assets/9b1439d3-d0ac-4eed-a073-916d13cc7cdc">

---

### StrategyPro
The core of the platform. Select strategies by market, tag, name, or performance metrics, then configure contract sizes and weightings to build a portfolio in seconds. Analyze individual systems or full portfolios with:

- Equity curves and drawdown charts
- Return distributions and bias analysis
- Correlation matrices between strategies
- Portfolio-level performance statistics

<img width="1052" alt="StrategyPro" src="https://github.com/user-attachments/assets/90bc639f-aac2-4ae8-b36e-69ba20c0bde7">

---

## Requirements

- Python 3.9+
- See [`requirements.txt`](requirements.txt) for the full dependency list

---

## License

This project is open-source and free to use.
