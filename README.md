# 📊 Pine Scripts Collection (TradingView)

![Pine Script](https://img.shields.io/badge/Pine%20Script-v6-brightgreen)
![TradingView](https://img.shields.io/badge/Platform-TradingView-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Status-Active-success)

A curated collection of **advanced TradingView Pine Script® v6 indicators** focused on:

- Liquidity & market structure
- Fibonacci & proprietary retracement levels
- Volume analysis (POC, participation)
- Multi-timeframe execution logic
- Institutional-style price action tools

Built for **serious traders, quants, and developers** who value clarity, structure, and reproducibility.

---

## 🚀 Features

- ✅ Pine Script **Version 6**
- ✅ Clean, modular, documented code
- ✅ Indicator-only (no auto trading)
- ✅ Crypto, Forex, Indices compatible
- ✅ Liquidity-first, confirmation-based logic

---

## 📁 Repository Structure

```text
pinescripts/
├── indicators/
│   ├── liquidity/
│   │   └── qps_liquidity_sweep.pine
│   ├── market-structure/
│   │   └── market_structure.pine
│   ├── fibonacci/
│   │   └── cc_fibonacci.pine
│   └── volume/
│       └── volume_poc.pine
│
├── strategies/
│   └── (optional future strategies)
│
├── libraries/
│   └── utils.pine
│
├── docs/
│   ├── methodology.md
│   ├── faq.md
│   └── screenshots/
│
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── STYLE_GUIDE.md
└── .gitignore
````

---

## 📌 Directory Overview

| Path                                                            | Description                 |
| --------------------------------------------------------------- | --------------------------- |
| [`indicators/`](./indicators)                                   | Core Pine Script indicators |
| [`indicators/liquidity/`](./indicators/liquidity)               | Liquidity sweeps & reclaims |
| [`indicators/market-structure/`](./indicators/market-structure) | Market structure tools      |
| [`indicators/fibonacci/`](./indicators/fibonacci)               | Fibonacci & CC levels       |
| [`indicators/volume/`](./indicators/volume)                     | Volume & POC indicators     |
| [`libraries/`](./libraries)                                     | Shared utilities            |
| [`docs/`](./docs)                                               | Methodology & FAQs          |

---

## 🧠 Methodology Philosophy

This repository emphasizes:

* **Reaction over prediction**
* **Liquidity before indicators**
* **Confirmation-based execution**
* **Invalidation-defined risk**

Most indicators follow this execution logic:

1. Liquidity sweep
2. Structural reclaim
3. Confirmation candle close
4. Clear technical invalidation

See full breakdown → [`docs/methodology.md`](./docs/methodology.md)

---

## 📦 Setup & Installation (TradingView)

### Option 1 — Manual (Recommended)

1. Open **TradingView**
2. Click **Pine Editor**
3. Click **New → Indicator**
4. Copy a `.pine` file from this repository
5. Paste it into the editor
6. Click **Save**
7. Click **Add to Chart**

---

### Option 2 — Organizing Multiple Indicators

For multiple indicators:

1. Create **separate scripts** in TradingView
2. Name them clearly (e.g. `QPS Liquidity Sweep`)
3. Keep utilities copied locally if TradingView library imports are not used

---

## 🧪 Supported Markets

* Bitcoin & Crypto
* Forex
* Indices
* Stocks (high liquidity preferred)

Recommended timeframes:

* **Higher TF:** 4H / Daily
* **Execution TF:** 5m / 15m / 30m

---

## 🤝 Contributing

Contributions are welcome.

Please read:

* [`CONTRIBUTING.md`](./CONTRIBUTING.md)
* [`STYLE_GUIDE.md`](./STYLE_GUIDE.md)

Rules:

* Pine Script **v6 only**
* No repainting unless clearly stated
* No obfuscation
* Clear variable names and comments

---

## ⚠️ Disclaimer

This project is for **educational and research purposes only**.
It is **not financial advice**.

Trading involves risk. You are responsible for your own decisions.

---

## 📜 License

Licensed under the **MIT License**.
See [`LICENSE`](./LICENSE) for details.

---

## ⭐ Support

If you find this useful:

* ⭐ Star the repository
* 🛠️ Open issues or pull requests
* 🧠 Share improvements