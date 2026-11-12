Tesla Stock Price Forecast Banner.png
# Tesla Stock Price Forecasting with Facebook Prophet

A Python time-series forecasting project that explores Tesla (TSLA) historical closing prices and builds a 30-calendar-day forecast using [Prophet](https://facebook.github.io/prophet/).

## Project overview

This repository contains a cleaned Jupyter Notebook based on the supplied project notebook. The original notebook expected a manually provided CSV file (`TSLA Historical Data (1).csv`), which was not included. To make the project easier to reproduce, the cleaned notebook downloads TSLA historical market data at runtime with `yfinance`.

### Workflow

1. Download historical TSLA market data from Yahoo Finance.
2. Inspect and clean the downloaded data with Pandas.
3. Visualize closing prices and trading volume with Plotly.
4. Format the data for Prophet (`ds` = date, `y` = closing price).
5. Fit a Prophet forecasting model.
6. Generate a 30-calendar-day forecast.
7. Visualize the forecast and trend components.
8. Export the forecast to CSV.

## Repository structure

```text
Tesla-Stock-Price-Prediction-Using-Prophet/
├── notebooks/
│   └── tesla_stock_forecasting_prophet.ipynb
├── data/
│   └── README.md
├── outputs/
│   └── .gitkeep
├── requirements.txt
├── .gitignore
└── README.md
```

## Requirements

- Python 3.9 or newer (a compatible Python environment is recommended)
- Internet connection to download market data
- Packages listed in `requirements.txt`

## Setup and run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Tesla-Stock-Price-Prediction-Using-Prophet.git
cd Tesla-Stock-Price-Prediction-Using-Prophet
```

### 2. Create and activate a virtual environment (recommended)

```bash
python -m venv .venv
```

Windows:

```bash
.venv\\Scripts\\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open `notebooks/tesla_stock_forecasting_prophet.ipynb` and run the cells from top to bottom.

You can also upload the notebook to Google Colab. If running from Colab, install the requirements in the first notebook cell and run the remaining cells in order.

## Output

The notebook saves:

- `data/TSLA_historical_data.csv` — downloaded historical data
- `outputs/TSLA_30_day_forecast.csv` — Prophet forecast output

These generated CSV files are excluded from Git by default. They can be recreated by running the notebook.

## Important limitations

- The original CSV was not provided; this version retrieves a replacement dataset online. Results may differ from those in the original run.
- Yahoo Finance data and availability can change.
- The 30-day horizon represents calendar days, not only stock-market trading days.
- The notebook does not include a formal train/test evaluation or backtesting. Forecast quality should not be assumed from the plotted output alone.
- This project is educational and is not investment advice.

## Technologies used

- Python
- Pandas
- yfinance
- Facebook Prophet
- Plotly
- Jupyter Notebook

## Acknowledgements

- [Prophet documentation](https://facebook.github.io/prophet/)
- [yfinance documentation](https://ranaroussi.github.io/yfinance/)
- [Yahoo Finance](https://finance.yahoo.com/)

---

If you find this project useful, feel free to star the repository.
