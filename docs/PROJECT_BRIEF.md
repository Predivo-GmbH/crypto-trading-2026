# Crypto Trading 2026 — Project Brief

## Overview
Personal crypto trading dashboard built to execute a disciplined accumulation strategy during the 2026 bear/consolidation phase and position for the expected 2027 bull cycle.

## Type
Personal tool — not a SaaS product. Single user (Roger).

## Tech Stack
- **Frontend:** React 19 + Vite + TailwindCSS
- **Backend:** FastAPI (Python)
- **Database:** Supabase (PostgreSQL + Auth)
- **AI:** Claude API for sentiment analysis and narrative detection
- **Deploy:** Vercel (frontend) + Supabase (DB + edge functions)

## Core Modules

### 1. DCA Engine
- Configure recurring buy schedules for BTC and selected alts
- Set rules: buy more aggressively below certain price thresholds (e.g., BTC < $60K = increase allocation)
- Track total accumulated, average cost basis, and unrealized P&L
- Integration with exchange API (Coinbase/Binance) for execution or manual logging

### 2. Halving Cycle Tracker
- Visual timeline showing current position in the 4-year BTC halving cycle
- Historical overlay: 2013, 2017, 2021 cycles with drawdown percentages
- Phase indicator: accumulation / markup / distribution / markdown
- Days since last halving, days to estimated peak based on historical patterns

### 3. Narrative & Sentiment Scanner
- AI-powered monitoring of key crypto narratives:
  - AI agents (AIXVT, Virtuals, agent wallets)
  - Meme coins (DOGE, SHIB, BONK, PENGU)
  - DeFi (yield protocols, buyback mechanisms — Hyperliquid, Pump)
  - RWA (real-world asset tokenization)
  - NFT resurgence signals
- Sentiment analysis from Twitter/X and Reddit
- Narrative strength score (1-10) with trend direction

### 4. Portfolio Dashboard
- Unified view of all crypto holdings across exchanges/wallets
- Allocation breakdown by narrative/category
- Performance tracking vs BTC benchmark
- Risk exposure visualization

### 5. Catalyst Calendar
- Key dates pre-loaded:
  - FOMC meetings (Mar 17, Apr 28, Jun 16, Jul 28, Sep 15, Oct 27, Dec 8)
  - US midterm elections (Nov 2026)
  - BTC halving anniversary markers
  - Major crypto events/conferences
- Custom event support
- Countdown timers for next catalyst
- Historical impact data (e.g., "avg 1-year return post-midterms: 15.4%")

## Key Data Sources
- **Price data:** CoinGecko or CoinMarketCap API (free tier)
- **On-chain data:** Glassnode or similar (free tier where available)
- **Social sentiment:** Twitter/X API, Reddit API, or aggregator like LunarCrush
- **Calendar data:** Manual + Fed calendar API
- **News:** CryptoPanic API or RSS feeds

## Investment Strategy (from research)
- BTC bottom expected May–October 2026
- Target accumulation zone: $30K–$60K
- DCA consistently through 2026
- Conservative BTC target: $160K–$180K (2027–2028)
- Diversify portion into stocks (AI, defense, health, pre-IPO)
- Key thesis: 4-year halving cycle + midterm election year stimulus + potential rate cuts

## Scope Guard — What This Is NOT
- Not a trading bot that auto-executes leveraged trades
- Not a SaaS product — no auth system for other users needed
- Not a social platform — no sharing/community features
- Not financial advice software — personal use only

## Architecture
```
┌─────────────────────────────────────────┐
│           React 19 Frontend             │
│  (Dashboard, Charts, Calendar, Config)  │
└──────────────┬──────────────────────────┘
               │ REST API
┌──────────────▼──────────────────────────┐
│           FastAPI Backend               │
│  ┌──────────┐ ┌───────────┐ ┌────────┐ │
│  │ DCA      │ │ Narrative │ │Calendar│ │
│  │ Engine   │ │ Scanner   │ │Service │ │
│  └──────────┘ └───────────┘ └────────┘ │
│  ┌──────────┐ ┌───────────┐            │
│  │ Portfolio│ │ Claude AI │            │
│  │ Tracker  │ │ Service   │            │
│  └──────────┘ └───────────┘            │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│          Supabase                       │
│  (PostgreSQL, Auth, Edge Functions)     │
└─────────────────────────────────────────┘
```
