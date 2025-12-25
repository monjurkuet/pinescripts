# Quantitative Pivot Strategy (QPS)

An advanced **liquidity-based Pine Script v6 indicator** combining:

- Fibonacci retracements
- Proprietary CC levels (0.66, 0.71)
- Liquidity sweep detection
- SR reclaim confirmation
- Volume validation
- Multi-timeframe trend alignment

---

## 📌 Core Logic

1. Identify key Fibonacci & CC levels
2. Detect liquidity sweeps beyond those levels
3. Require reclaim confirmation (optional)
4. Validate with volume & HTF trend
5. Generate clean long / short signals

---

## ⚙️ Key Inputs

- **Reclaim Mode** – confirmation-based vs sweep-only entries
- **CC Levels** – configurable proprietary retracement zones
- **Volume Threshold** – filters low-quality moves
- **HTF Alignment** – directional bias control

---

## 🧪 Best Use Cases

- BTC / ETH
- Forex majors
- Indices
- 5m–30m execution with 4H / Daily HTF

---

## ⚠️ Notes

- Designed for **reaction, not prediction**
- Avoid low-liquidity assets
- Works best in corrective & range environments
