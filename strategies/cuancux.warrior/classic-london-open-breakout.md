---
name: Classic London Open Breakout
owner: cuancux.warrior
symbol: XAUUSD
timeframe: H1
session: LONDON_OPEN
trigger: breakout
direction: AUTO
params:
  lookback: 8
  min_range_atr_mult: 0.3
sl:
  mode: ATR
  mult: 1.5
tp:
  rr: 2.0
enabled: true
auto: false
version: '1.0'
---

Classic London Open Breakout — see DRAFT §23 rules engine.
