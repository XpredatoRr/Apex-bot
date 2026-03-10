# CLAUDE.md — Apex-bot Repository Guide

## Project Overview

**Apex-bot** is a repository for a high-frequency trading (HFT) simulator concept called **"APEX HFT Speculator"**. The current state of the repository contains a visual design reference/specification document rather than functional application code.

The project is focused on a cryptocurrency trading simulator with educational intent — simulated trades only, no real money.

---

## Repository Structure

```
Apex-bot/
├── README.md               # Minimal project title only
├── CLAUDE.md               # This file
└── apex-speculator.html    # PDF-converted-to-HTML design specification/mockup
```

### File Descriptions

| File | Description |
|------|-------------|
| `README.md` | Placeholder README with project name only |
| `apex-speculator.html` | Visual UI mockup of the APEX HFT Speculator dashboard, originally a PDF converted to HTML via pdf24. Contains embedded base64 fonts (Orbitron, ShareTechMono, Menlo). |

---

## Project Concept & Features (from design spec)

The `apex-speculator.html` documents the intended interface and feature set:

### Dashboard Sections
- **LIVE TRADE FEED** — Real-time trade activity stream
- **PORTFOLIO** — Asset holdings overview
- **TRADES** — Trade history and activity
- **STRATS** — Strategy configuration
- **LEARN** — Educational content
- **NEWS** — Market news feed
- **MARKET** — Market data view

### Trading Parameters
- Balance display (USDT denominated)
- Profit/Loss tracking with percentage
- Win Rate metric
- Trades per minute (10/min, 55/min, 100/min modes)
- Position Size (%)
- Stop Loss (%)
- Take Profit (%) — e.g. 1.5%, 2.5%
- Trade Frequency control

### Supported Cryptocurrencies
BTC, ETH, SOL, ADA, BNB, MATIC, AVAX, DOT, LINK, LTC, UNI, ARB, OP, ATOM, FIL, ICP, NEAR, APT

### Unique Features
- **HALAL FILTER**: Permanently blocks riba, gambling, and haram tokens
- **AI Integration**: "LAUNCH AI" capability
- **Gamification**: XP/Level system (e.g., "9999 / 1500 XP", "L6"), performance rating
- **Status indicators**: OFFLINE, LOADING, etc.

### Design Theme
- Color scheme: Teal/cyan (`#00ABA5`, `#00AAA4`) on dark background, gold (`#AB9600`) accents, green (`#00AB5B`) for positive metrics
- Fonts: Orbitron (headings), ShareTechMono (data/metrics), Menlo (secondary)
- Style: Terminal/HFT aesthetic

> **Important disclaimer from the spec:** "⚠ SIMULATION ONLY. Fake money. No real trades. For education only."

---

## Development Status

| Aspect | Status |
|--------|--------|
| Source code | **Not yet created** |
| Backend | **Not yet created** |
| Frontend | **Not yet created** (only static mockup exists) |
| Database | **Not yet created** |
| Tests | **Not yet created** |
| CI/CD | **Not yet created** |
| Package management | **Not yet created** |

The repository is in an early planning/design phase.

---

## Git Information

- **Default branch**: `master`
- **Remote**: `http://local_proxy@127.0.0.1:41241/git/XpredatoRr/Apex-bot`
- **Owner**: XpredatoRr

### Commit History
```
a92b46d  Delete apex-speculator.pdf
0acb012  Add files via upload (HTML conversion)
601e7b8  Add files via upload (original PDF)
7a6650e  Initial commit (README.md)
```

---

## Guidance for AI Assistants

### When asked to implement the bot

If asked to build the actual trading simulator, consider this recommended stack based on the project concept:

- **Frontend**: React or Vue.js with a dark-themed component library (e.g., shadcn/ui, Radix)
- **Backend**: Node.js/Express or FastAPI (Python) for trade simulation logic
- **Real-time data**: WebSockets for live feed simulation
- **State management**: Zustand or Redux for portfolio/trade state
- **Charting**: TradingView Lightweight Charts or Recharts
- **Database**: PostgreSQL or SQLite for trade history

### Key conventions to follow (when code is added)
1. **Simulation only** — never implement real trade execution or connection to live exchange APIs with real funds
2. **Halal compliance** — the halal filter is a core feature; maintain the blocked-token list
3. **Educational focus** — UI should clearly communicate that this is a simulator
4. **Disclaimer visibility** — always show the simulation disclaimer prominently

### When modifying `apex-speculator.html`
- This file is a converted PDF (pdf24 format) — it uses absolute positioning and embedded base64 fonts
- It is not a standard editable HTML template; treat it as a static reference asset
- Do not attempt to refactor it into a functional web app — create separate source files instead

### File creation guidance
When the project moves to active development, create:
```
src/
├── components/    # UI components
├── hooks/         # Custom React hooks
├── services/      # Trading simulation logic
├── store/         # State management
└── utils/         # Helpers (halal filter, formatters, etc.)
```

---

## No Build System Yet

There are currently no build scripts, test runners, linters, or package managers configured. When adding them, document the commands here.

---

*Last updated: 2026-03-10*
