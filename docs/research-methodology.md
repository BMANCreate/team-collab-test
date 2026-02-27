# Research Methodology

**Role:** Research Analyst (Boy)  
**Team:** Investment Team  
**Last Updated:** 2026-02-26

---

## Overview

This document outlines the research process, data sources, and quality standards used by the Investment Team's research function. The goal is to produce timely, accurate, and actionable investment research that supports BMAN's decision-making.

---

## Research Process

### 1. Signal Intake
- Receive signals from Roey (Coordinator) classified as Red / Yellow / Green
- Red signals → immediate deep-dive initiated
- Yellow signals → added to the daily research queue
- Green signals → auto-archived, reviewed weekly

### 2. Initial Screening (< 2h)
- Token/project basics: category, chain, market cap, launch date
- Team background and funding history
- Community size and sentiment (Twitter, Discord, Telegram)
- On-chain metrics: TVL, active addresses, transaction volume

### 3. Due Diligence (1–3 days for Yellow; same-day for Red)
- **Tokenomics analysis**: supply schedule, vesting, inflation rate
- **Competitive landscape**: comparable projects, differentiation
- **On-chain deep dive**: whale wallets, holder concentration, DEX liquidity
- **Risk assessment**: smart contract audits, regulatory exposure, team anonymity
- **Narrative fit**: alignment with current market cycle themes

### 4. Backtesting (when applicable)
- Historical price performance vs. BTC/ETH
- Drawdown analysis across prior market cycles
- Entry/exit signal testing using defined criteria

### 5. Report Production
- Summary: 1-paragraph TL;DR
- Recommendation: BUY / WATCH / PASS + rationale
- Key risks: top 3 risks with severity rating
- Data appendix: raw data tables and charts

---

## Data Sources

| Category | Sources |
|----------|---------|
| On-chain | Dune Analytics, Nansen, Glassnode, DefiLlama |
| Market data | CoinGecko, CoinMarketCap, TradingView |
| News & narrative | Crypto Twitter, The Block, Decrypt, Messari |
| Social sentiment | LunarCrush, Santiment, Reddit |
| Developer activity | GitHub, Electric Capital Dev Report |
| Regulatory | Chainalysis, compliance databases |

---

## Research Output Formats

### 1. Flash Report (Red Signal, < 4h)
- 1-page max
- Recommendation + top 3 data points
- Immediate sharing to Roey and BMAN

### 2. Standard Report (Yellow Signal, 1–3 days)
- Full due diligence document
- Shared in `#research` channel on BotsHub
- Stored as artifact in the relevant thread

### 3. Weekly Digest (Every Monday 10:00 SGT)
- Summary of all research completed in the prior week
- Market theme updates
- Watchlist changes

---

## Sharing & Collaboration

- All research artifacts are posted in the **#research** channel on BotsHub (boot.hxa.net)
- Major reports are attached as thread artifacts in BMAN Team Collaboration
- Roey receives all Red/Yellow signal reports directly
- Joey has access to raw data for modeling purposes
- zylos-abcde receives reports for compliance and risk audit

---

## Quality Standards

| Standard | Requirement |
|----------|-------------|
| Timeliness | Red: < 4h · Yellow: < 72h · Green: weekly |
| Source citation | All claims must cite at least 1 primary source |
| Bias check | Disclose any potential conflicts of interest |
| Peer review | All Standard Reports reviewed by Roey before delivery |
| Versioning | Reports are versioned (v1, v2…) when updated |

---

## Escalation Protocol

- **If data is conflicting or insufficient:** flag to Roey, pause research, request more time
- **If Red signal requires BMAN decision within 1h:** send Flash Report immediately, continue deeper analysis in parallel
- **If security/compliance issue found:** escalate to zylos-abcde simultaneously with Roey

---

*This document is maintained by Boy. Updates require Roey approval.*
