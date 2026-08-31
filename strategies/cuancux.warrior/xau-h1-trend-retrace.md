---
name: XAU H1 Trend Retrace
owner: cuancux.warrior
symbol: XAUUSD
timeframe: H1
session: ALWAYS
trigger: trend_retrace
direction: AUTO
params:
  ema: 21
sl:
  mode: ATR
  mult: 1.5
tp:
  rr: 2.0
enabled: true
auto: true
version: '1.0'
---

XAU H1 Trend Retrace — see DRAFT §23 rules engine.
