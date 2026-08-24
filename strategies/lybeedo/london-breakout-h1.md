---
name: London Breakout H1
owner: lybeedo
symbol: XAUUSD
timeframe: H1
session: LONDON_OPEN
trigger: breakout
direction: AUTO
params:
  range_hours: 2
  atr_mult: 1.5
sl: 12
tp: 26
enabled: true
auto: false
version: "1.0"
---
Classic London open breakout: define the first 2h range, enter on a break with
1.5×ATR stop. Works best in high-volatility Asian→London transitions. Only take
the first break of the session; skip if the range is < 0.3×ATR.
