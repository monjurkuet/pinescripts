# Complete Guide: How to Use the Quantitative Pivot Strategy (QPS) Indicator

---

## 📥 INSTALLATION

### Step 1: Add to TradingView
1. Open TradingView → Pine Script Editor (bottom panel)
2. Delete any existing code
3. Paste the full indicator code
4. Click **"Add to Chart"**
5. The indicator will appear on your chart

---

## 🎯 UNDERSTANDING THE VISUAL ELEMENTS

### On-Chart Elements

| Element | Color | Meaning |
|---------|-------|---------|
| **Golden Line (thick)** | 🟡 Yellow | 0.618 Golden Pocket - Retail liquidity zone |
| **Orange Line** | 🟠 Orange | CC Level (0.66) - First institutional zone |
| **Red Line (thickest)** | 🔴 Red | CC 3.0 Level (0.71) - Deep liquidity zone |
| **Blue Dots** | 🔵 Blue | Volume POC (Point of Control) |
| **Green/Red Boundaries** | Light | Current range high/low |
| **White Line** | ⚪ White | 50 SMA (trend direction) |

### Signal Shapes

| Shape | Location | Meaning |
|-------|----------|---------|
| **Purple Circle** | Above/Below bars | Liquidity sweep detected |
| **Small Diamond** | Above/Below bars | Awaiting reclaim confirmation |
| **Large Triangle UP** | Below bar | ✅ **LONG ENTRY SIGNAL** |
| **Large Triangle DOWN** | Above bar | ✅ **SHORT ENTRY SIGNAL** |

### Background Colors

| Color | Meaning |
|-------|---------|
| **Light Green BG** | Bullish sweep active - watching for reclaim |
| **Light Red BG** | Bearish sweep active - watching for reclaim |
| **Brighter Green BG** | Long entry triggered |
| **Brighter Red BG** | Short entry triggered |

---

## 📊 THE INFO TABLE (Top Right)

```
┌─────────────────────┬──────────────┐
│ QPS STATUS          │ VALUES       │
├─────────────────────┼──────────────┤
│ Current Trend       │ ▲ BULLISH    │  ← Based on 50 SMA
│ HTF Trend (240)     │ ▲ BULLISH    │  ← 4H timeframe trend
│ 0.618 Golden Pocket │ 95,234.50    │  ← Key retail level
│ CC (0.66)           │ 94,123.00    │  ← First CC level
│ CC 3.0 (0.71)       │ 93,456.00    │  ← Deep liquidity
│ Volume POC          │ 96,100.00    │  ← High volume node
│ Bull Sweep Active   │ ● YES        │  ← Sweep happened
│ Bear Sweep Active   │ ○ NO         │  ← No bear sweep
│ Reclaim Progress    │ 1 / 2        │  ← 1 of 2 confirms
│ Volume Status       │ ⬆ HIGH       │  ← Above average
│ SIGNAL              │ ◔ AWAIT...   │  ← Current state
└─────────────────────┴──────────────┘
```

---

## 🔄 THE COMPLETE TRADING WORKFLOW

### Phase 1: Preparation (Before Trading)

```
1. Set your timeframe:
   - RECOMMENDED: 30m or 4H charts
   - Higher TF (4H/Daily) for bias
   - Lower TF (30m) for entries

2. Check the table:
   - Current Trend = Your bias direction
   - HTF Trend = Must align for high-probability trades
```

### Phase 2: Wait for Sweep (The Setup)

```
WHAT YOU'RE LOOKING FOR:

For LONGS:
┌──────────────────────────────────┐
│    Price approaching from above  │
│              ↓                   │
│    ══════ 0.618 Level ══════    │
│              ↓                   │
│    ══════ 0.66 CC Level ══════  │
│              ↓                   │
│    ══════ 0.71 CC 3.0 ══════    │
│         ╲   │   ╱                │
│          ╲  │  ╱  ← WICK pierces │
│           ╲ │ ╱     below level  │
│            ╲│╱                   │
│             V                    │
│    Price closes BACK ABOVE       │
│    = LIQUIDITY SWEEP ✓           │
└──────────────────────────────────┘

For SHORTS:
(Opposite - wick pierces ABOVE then closes back below)
```

**When sweep happens:**
- Purple circle appears
- Background turns light green/red
- Table shows "Bull/Bear Sweep Active: ● YES"
- Table shows "SIGNAL: ◔ AWAIT RECLAIM"

### Phase 3: Confirmation (The Trigger)

```
RECLAIM CONFIRMATION PROCESS:

Candle 1: Closes above the level    → Count: 1/2
Candle 2: Closes above the level    → Count: 2/2 ✓
                                      
         ═══════════════════════
         ▲ LEVEL RECLAIMED
         
After 2 consecutive closes above level:
→ LONG ENTRY SIGNAL (Green Triangle)
```

**What the indicator shows:**
- "Reclaim Progress" in table counts up
- When complete: Large triangle appears
- Bar turns green (long) or red (short)
- Brighter background flash

### Phase 4: Entry Execution

```
WHEN YOU SEE THE TRIANGLE:

✅ ENTER THE TRADE on the CLOSE of that candle
   (Don't chase - wait for candle to complete)

📍 STOP LOSS:
   - Automatically shown as dashed red line
   - Placed just below the sweep low (for longs)
   - Placed just above the sweep high (for shorts)
```

### Phase 5: Trade Management

```
TARGET IDENTIFICATION:

1st Target: Next Fibonacci level above/below
2nd Target: Volume POC level
3rd Target: Range high/low

TRAILING APPROACH:
- Move SL to breakeven after 1R profit
- Trail below/above each reclaimed level
```

---

## ⚙️ RECOMMENDED SETTINGS BY MARKET

### For Bitcoin/Crypto (High Volatility)

| Setting | Value | Reason |
|---------|-------|--------|
| Fibonacci Lookback | 100 | Captures major swings |
| CC Level 1 | 0.66 | Standard |
| CC Level 2 | 0.71 | Deep liquidity |
| Sweep Buffer % | 0.15 | Accounts for spread |
| Min Wick % | 50 | Ensures real sweeps |
| Confirmation Candles | 2 | Balance of speed/safety |
| Volume Threshold | 1.5x | Confirms participation |
| HTF for Trend | 240 (4H) | Good for swing trades |

### For Forex (Lower Volatility)

| Setting | Value | Reason |
|---------|-------|--------|
| Fibonacci Lookback | 50 | Tighter ranges |
| Sweep Buffer % | 0.10 | Tighter spreads |
| Min Wick % | 40 | More frequent setups |
| Confirmation Candles | 1 | Faster confirmation |
| Volume Threshold | 1.3x | Less volume variation |

### For Stocks/Indices

| Setting | Value | Reason |
|---------|-------|--------|
| Fibonacci Lookback | 80 | Medium swings |
| Sweep Buffer % | 0.20 | Gap protection |
| Confirmation Candles | 2 | Standard |
| HTF for Trend | D (Daily) | Follows institutions |

---

## 📋 TRADE CHECKLIST

Before every trade, confirm:

```
□ 1. SWEEP OCCURRED
     Purple circle appeared?
     Background color changed?

□ 2. HTF ALIGNMENT
     Table shows HTF trend matches trade direction?
     (Bull for longs, Bear for shorts)

□ 3. RECLAIM CONFIRMED  
     Triangle signal appeared?
     Reclaim Progress shows complete?

□ 4. VOLUME PRESENT
     Volume Status shows "HIGH"?
     (Or acceptable if "NORMAL")

□ 5. STOP LOSS IDENTIFIED
     Dashed line visible?
     Risk acceptable for position size?

□ 6. TARGET IDENTIFIED
     Know your 1R, 2R, 3R targets?

ALL BOXES CHECKED? → EXECUTE TRADE
```

---

## 🎓 TRADING SCENARIOS

### Scenario 1: Perfect Long Setup

```
CHART SITUATION:
- 4H trend: Bullish ✓
- Price drops into CC zone (0.66-0.71)
- Long wick pierces below 0.71
- Candle closes back above 0.66
- Purple circle appears ✓
- Next 2 candles close above 0.66
- Green triangle appears ✓
- Volume is HIGH ✓

ACTION:
→ Enter LONG at triangle candle close
→ Stop Loss: Below the sweep wick low
→ Target 1: 0.618 level
→ Target 2: 0.50 level  
→ Target 3: Range high
```

### Scenario 2: Short Setup in Downtrend

```
CHART SITUATION:
- 4H trend: Bearish ✓
- Price rallies into resistance
- Wick pierces above 0.618
- Candle closes back below
- Purple circle appears ✓
- Next 2 candles close below
- Red triangle appears ✓

ACTION:
→ Enter SHORT at triangle candle close
→ Stop Loss: Above the sweep wick high
→ Targets: CC levels below, then range low
```

### Scenario 3: No Trade (Filtered Out)

```
CHART SITUATION:
- 4H trend: Bullish
- Sweep occurs at CC level ✓
- BUT: Reclaim fails (price drops again)
- Reclaim Progress resets to 0/2

RESULT:
→ NO SIGNAL generated
→ NO TRADE taken
→ System protected you from fakeout
```

---

## ⚠️ COMMON MISTAKES TO AVOID

### ❌ Mistake 1: Entering on the Sweep
```
WRONG: Buying immediately when purple circle appears
RIGHT: Wait for reclaim confirmation (triangle)
```

### ❌ Mistake 2: Ignoring HTF Trend
```
WRONG: Taking long signals when HTF shows BEARISH
RIGHT: Only take longs when HTF aligns bullish
       (Or disable "Require HTF Alignment" for counter-trend)
```

### ❌ Mistake 3: Moving Stop Loss
```
WRONG: Moving SL further away when price goes against you
RIGHT: Keep SL at invalidation (below sweep low)
       If it hits, the setup was wrong
```

### ❌ Mistake 4: Over-Trading
```
WRONG: Taking every signal regardless of context
RIGHT: Focus on signals at major CC levels (0.66, 0.71)
       Ignore signals at standard 0.618 (more retail noise)
```

### ❌ Mistake 5: Wrong Timeframe
```
WRONG: Using 1-minute chart for swing trades
RIGHT: Match timeframe to your trading style:
       - Scalping: 5m-15m
       - Day Trading: 30m-1H
       - Swing Trading: 4H-Daily
```

---

## 📐 POSITION SIZING FORMULA

```
CALCULATE YOUR POSITION SIZE:

Risk Amount = Account Balance × Risk %
            = $10,000 × 1%
            = $100

Stop Distance = Entry Price - Stop Loss
              = $95,000 - $94,200
              = $800 (0.84%)

Position Size = Risk Amount ÷ Stop Distance %
              = $100 ÷ 0.84%
              = $11,905 position value

For leveraged trading:
Contracts = Position Size ÷ Entry Price
          = $11,905 ÷ $95,000
          = 0.125 BTC
```

---

## 🔔 SETTING UP ALERTS

### Step 1: Click on the indicator name → "Add Alert"

### Step 2: Choose condition:

| Alert | When to Use |
|-------|-------------|
| "Bullish Liquidity Sweep" | Get notified when setup begins |
| "Bearish Liquidity Sweep" | Get notified when setup begins |
| "Long Entry Signal" | Get notified to enter long |
| "Short Entry Signal" | Get notified to enter short |
| "Any Entry Signal" | Get all entry alerts |

### Step 3: Set notification method
- Push notification (mobile)
- Email
- Webhook (for bots)

---

## 📈 BACKTESTING THE STRATEGY

### Manual Backtest Process:

```
1. Go back 6+ months on your chart
2. Hide the indicator signals temporarily
3. Scroll forward bar-by-bar
4. Mark each signal that would have triggered
5. Calculate:
   - Win Rate = Wins ÷ Total Trades
   - Average R = Total R ÷ Total Trades
   - Expectancy = (Win% × Avg Win) - (Loss% × Avg Loss)

TARGET METRICS:
- Win Rate: 45-55% is acceptable
- Average R:R: 2:1 or better
- Expectancy: Positive
```

---

## 🎯 QUICK REFERENCE CARD

```
╔══════════════════════════════════════════════════╗
║          QPS QUICK REFERENCE                     ║
╠══════════════════════════════════════════════════╣
║                                                  ║
║  LONG ENTRY RULES:                               ║
║  ✓ Price sweeps below 0.618/0.66/0.71           ║
║  ✓ Closes back above the level                  ║
║  ✓ 2 consecutive closes above (reclaim)         ║
║  ✓ Volume above average                         ║
║  ✓ HTF trend bullish                            ║
║  → Green triangle = ENTER LONG                  ║
║  → Stop: Below sweep low                        ║
║                                                  ║
║  SHORT ENTRY RULES:                              ║
║  ✓ Price sweeps above 0.618/0.66/0.71           ║
║  ✓ Closes back below the level                  ║
║  ✓ 2 consecutive closes below (reclaim)         ║
║  ✓ Volume above average                         ║
║  ✓ HTF trend bearish                            ║
║  → Red triangle = ENTER SHORT                   ║
║  → Stop: Above sweep high                       ║
║                                                  ║
║  KEY LEVELS (most to least important):          ║
║  1. 0.71 CC 3.0 (RED) - Best setups            ║
║  2. 0.66 CC (ORANGE) - Good setups             ║
║  3. 0.618 GP (YELLOW) - Retail zone            ║
║                                                  ║
╚══════════════════════════════════════════════════╝
```

---

## 💡 PRO TIPS

1. **Best setups occur at CC 3.0 (0.71)** - This is where institutions hunt liquidity

2. **Multiple sweeps = stronger signal** - If price sweeps twice, the reversal is more likely

3. **Combine with market structure** - Look for sweeps at swing lows/highs

4. **Time of day matters** - Avoid signals during low-liquidity periods

5. **News awareness** - Don't trade signals right before major news events

6. **Journal your trades** - Track which levels work best for your market

---