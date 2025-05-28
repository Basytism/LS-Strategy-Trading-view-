📈Instinct Edge v2 — Refined Accuracy
A refined multi-confirmation trading strategy based on moving average crossovers, volume behavior, RSI trend confirmation, and price range compression. Designed to improve entry precision and filter out false signals by incorporating smart volatility and stability filters.

🔧 Strategy Overview
This strategy enters trades based on:

SMA Crossover: Bullish or bearish cross between fast and slow SMAs.

Volume Breakout Confirmation: Ensures price moves are backed by significant volume.

RSI Trend Filter: Confirms that the market is in a trending condition.

Order Block Filter: Avoids trades during tight price ranges or when volume is unstable.

⚙️ Input Parameters
Parameter	Description	Default
Fast SMA Length	Period for the fast-moving average	14
Slow SMA Length	Period for the slow-moving average	28
RSI Length	RSI period used for trend confirmation	14
RSI Threshold	Minimum RSI value to confirm bullish trend (or 100 - X for bearish)	50
Volume Lookback	Period to analyze average and stability of volume	12
ATR Length	ATR period used to measure volatility	14
ATR Filter Multiplier	Controls price range compression sensitivity	1.0
Breakout Volume Multiplier	Triggers only on high volume spikes	1.5
Min Reward/Risk	Reserved for future implementation (RR filtering)	1.5

✅ Entry Logic
Long Entry (BUY) occurs when:

Fast SMA crosses above Slow SMA.

RSI is above the threshold (e.g., 50).

Volume exceeds 1.5× its recent average.

Price is not in a tight, low-volatility range.

Short Entry (SELL) occurs when:

Fast SMA crosses below Slow SMA.

RSI is below the inverted threshold (e.g., 50 → 100-50 = 50).

Volume exceeds 1.5× average.

Market is not in a compressed price block (order block zone).

