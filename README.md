# Public Strategy Database

**Jarwo AI Assistant** — user-contributed trading strategies, readable by anyone, writable by their owners.

Structure:

```
strategies/<owner>/<slug>.md
```

Each strategy is a Markdown file with YAML frontmatter + optional prose. The Jarwo engine
(`Lybeedo/jarwo-bot`) lists this repo, parses the rules, and imports them into a user's
local rule store. Users never overwrite another owner's file.

## Rule format

```yaml
---
name: London Breakout H1
owner: lybeedo
symbol: XAUUSD
timeframe: H1
session: LONDON_OPEN
trigger: breakout
direction: both
params:
  range_hours: 2
  atr_mult: 1.5
sl: 12
tp: 26
enabled: true
auto: false
version: "1.0"
---
Prose describing the idea, rationale, and any notes.
```

## Adding a strategy

Fork this repo → add `strategies/<your-owner>/<slug>.md` → open a PR (or push directly if
you're a Lybeedo member). The engine picks it up on its next refresh (TTL ~5 min).

## Env in the engine

| Variable | Default |
|---|---|
| `JARWO_STRATEGY_REPO` | `Lybeedo/public-strategy-database` |
| `JARWO_STRATEGY_BRANCH` | `main` |
| `JARWO_STRATEGY_PATH` | `strategies` |

See `Lybeedo/jarwo-bot` → `docs/STRATEGIES.md` for the full spec.
