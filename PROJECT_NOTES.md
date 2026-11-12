# Project notes

## Source notebook adaptation

The uploaded notebook described Tesla (TSLA) stock price prediction using Facebook Prophet. Its workflow included data import, exploratory analysis, Plotly visualizations, Prophet data preparation (`Date`/`Price` renamed to `ds`/`y`), model fitting, a 30-period forecast, forecast plotting, component plotting, and CSV export.

The supplied notebook depended on a local file named `TSLA Historical Data (1).csv`. That file was not included. This repository therefore uses `yfinance` to fetch a replacement TSLA dataset when the notebook runs. The fetched data is not represented as the exact original dataset.

## Reproducibility

Run the notebook from top to bottom in an environment with internet access. The data provider may revise or limit historical data, so outputs can change between runs.
