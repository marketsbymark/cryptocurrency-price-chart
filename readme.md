# Cryptocurrency Price Chart

A static JavaScript page for viewing cryptocurrency price history and market-share charts, using bundled jQuery and Highstock assets.

This repository is a fork of [athlona64/cryptocurrency-price-chart](https://github.com/athlona64/cryptocurrency-price-chart). The original project attribution and license statement are preserved below.

## Run locally

No package installation or build step is included. With Python 3 installed, serve the repository directory:

```sh
git clone https://github.com/marketsbymark/cryptocurrency-price-chart.git
cd cryptocurrency-price-chart
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/` in a browser. Stop the local server with Ctrl+C.

The page offers currency-pair selection, time ranges, market-share display, and an optional average overlay. Selections are stored in the URL fragment; for example, `#BTC/USDT:1y`.

## Data dependencies and limitations

The page loads market data over the network. The checked-in source uses Poloniex's `returnChartData` endpoint and legacy CoinMarketCap graph endpoints through a third-party proxy at `nexunity.org`. These external services are not bundled, and their current availability or compatibility is not guaranteed.

If the page remains on “Loading” or shows no data, inspect the browser's Network and Console panels for API, proxy, or cross-origin failures. Serving the files locally does not restore an unavailable data provider. This repository has no backend, replacement data feed, or automated test suite.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page layout, selectors, API requests, and chart logic |
| `jquery-1.10.1.min.js` | Bundled jQuery |
| `highstock.js` | Bundled charting library |
| `theme.js` | Chart theme |

## Original project references

Data provider: https://poloniex.com, https://coinmarketcap.com

Chart library: https://www.highcharts.com

Original live-version link: https://trustable-code.github.io/cryptocurrency-price-chart/ (external deployment; availability not verified).

License
-------

Cryptocurrency Price Chart is FLOSS (free and open-source software).<br>
All files in this repository are licensed under the [GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0) (GPLv3).<br>
Copyright 2017 Simon Krauter
