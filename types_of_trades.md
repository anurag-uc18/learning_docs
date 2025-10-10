# 🧭 Types of Trades & Strategies (Professional Overview)

## 1️⃣ By Trading Logic / Strategy Family

### 🌀 A. Mean-Reversion Trades
**Logic:** Prices revert to their mean after moving too far.  
**Used In:** Stocks, options, futures, pairs trading, volatility spreads.  
**Setup:** Buy oversold / sell overbought using RSI, Bollinger Bands, or z-score.  
**Example:** Buy SPY when 2 SD below 20-day MA and RSI < 30.  
**Used by:** Market-makers, stat-arb desks, high-frequency traders.

---

### 📈 B. Momentum / Trend-Following Trades
**Logic:** What’s moving tends to keep moving.  
**Used In:** Swing, position, and macro trading.  
**Setup:** Buy breakouts, use MA crossovers, ADX, or Donchian Channels.  
**Example:** Go long when 10-day MA crosses above 50-day MA.  
**Used by:** CTAs, hedge-fund “trend” systems.

---

### 💥 C. Breakout Trades
**Logic:** Volatility expands after key level breaks.  
**Used In:** Stocks, options, forex, futures.  
**Setup:** Enter on price/volume breakout from consolidation.  
**Example:** Long NVDA above $1200 with volume ≥ 2× average.  
**Variant:** Fade failed breakouts (reversion).

---

### 🔁 D. Range-Bound / Swing Trades
**Logic:** Trade oscillations between support/resistance.  
**Setup:** Buy near support, sell near resistance.  
**Example:** Buy AAPL ≈ $210, sell ≈ $220 repeatedly.  
**Overlap:** Hybrid of mean-reversion + technical.

---

### ⚖️ E. Arbitrage Trades
**Logic:** Exploit mispricing between related instruments.  
**Types:**
- **Stat Arb:** Long Coke / short Pepsi  
- **Merger Arb:** Buy target, short acquirer  
- **Triangular Arb:** 3-currency forex mispricing  
- **Convertible Arb:** Long convert bond, short stock  
**Used by:** Quant & prop desks, HFTs.

---

### 💰 F. Carry / Yield Trades
**Logic:** Capture yield or implied-volatility differentials.  
**Used In:** FX, bonds, options, crypto.  
**Example:** Long high-yield currency, short low-yield one.  
**Risk:** Small daily gains + occasional large losses.

---

### 📅 G. Event-Driven Trades
**Logic:** Trade predictable reactions to scheduled events.  
**Used In:** Stocks, options.  
**Examples:**  
- Earnings IV crush  
- Fed meeting vol plays  
- FDA approvals, M&A bets  
**Used by:** Event-driven hedge funds.

---

### 🌪️ H. Volatility / Options Trades
**Logic:** Trade volatility directly.  
**Examples:**
- Long vol → buy straddles/strangles  
- Short vol → sell premium for theta decay  
- Skew trades → exploit call/put IV differences  
- Calendar spreads → term-structure plays

---

### 🏦 I. Market-Making / Liquidity Provision
**Logic:** Quote bid/ask, profit from spread.  
**Used by:** Professional desks & algos.  
**Risk:** Inventory imbalance on sharp moves.

---

### 🤖 J. Quant / Machine-Learning Trades
**Logic:** Data-driven signals and factor models.  
**Examples:** 
- Buy stocks with positive earnings revisions + low vol  
- Predict next-day returns with ML features (RSI, volume, sentiment)

---

## 2️⃣ By Time Horizon

| Horizon | Trade Type | Holding Period |
|----------|-------------|----------------|
| ⚡ Scalp | Micro mean-reversion, liquidity | Seconds – Minutes |
| 💻 Day Trade | Intraday momentum / breakout / fade | Minutes – Hours |
| 📆 Swing | Mean-reversion / event / range | Days – Weeks |
| 🧭 Position | Trend-following / macro | Weeks – Months |
| 🏦 Investment | Fundamental / value | Months – Years |

---

## 3️⃣ By Options Structure (for Options Traders)

| Type | Core Idea |
|------|-----------|
| Directional (calls/puts) | Simple bullish / bearish bet |
| Credit Spreads | Sell premium with defined risk |
| Debit Spreads | Buy directional exposure with limited risk |
| Iron Condor / Butterfly | Range-bound, short-vol bet |
| Straddle / Strangle | Volatility (big move) bet |
| Calendar Spread | Volatility term-structure play |
| Ratio / Backspread | Skew or tail-hedge structure |

---

## 4️⃣ How Pros Blend Them
Professional traders rarely use only one style:  
- **Trend models** → capture big moves  
- **Mean-reversion** → harvest daily noise  
- **Options overlays** → hedge volatility or express macro bias  
- **Event plays** → enhance returns on key days  

---

✅ **Tip:**  
Pair this cheat-sheet with your own backtest logs.  
Add columns like “Strategy Type”, “Indicator”, “Entry Logic”, and “Exit Logic” to analyze what works best for you.

---

> 📎 *Contributions welcome!* Add new trade types or examples via pull request.
