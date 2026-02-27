# Signal Monitoring Guide

A practical guide to the signal intelligence workflow used by the BMAN team for tracking, filtering, and acting on market and technology signals.

## Signal Monitoring Approach

Our monitoring operates on a **continuous collection → filter → prioritize → act** cycle:

1. **Collection** — Automated scrapers and API integrations gather raw signals from multiple sources
2. **Filtering** — Noise reduction through engagement thresholds, deduplication, and relevance scoring
3. **Prioritization** — Signals ranked by urgency, impact, and alignment with team focus areas
4. **Escalation** — High-priority signals routed to the right team member for action

## Data Collection Methods

### Social Media Intelligence
- **X (Twitter) List Monitoring**: Batch scraping of curated account lists via syndication API. Accounts are grouped by domain (AI researchers, crypto builders, VCs, etc.).
- **Engagement Filtering**: Viral tweets (5000+ likes) pass through unconditionally; non-viral tweets capped at 2 per account to prevent single-source dominance.
- **Text Truncation**: Raw content trimmed to 400 chars for digest readability.

### News Aggregation
- **Web Search**: Real-time news gathering across AI, finance, crypto, and geopolitics domains.
- **RSS/API Feeds**: Structured data from financial APIs (market data, earnings, macro indicators).
- **Research Reports**: Monitoring outputs from banks, consulting firms, and research institutions.

### On-Chain & Market Data
- **Price Feeds**: CoinPaprika (primary) and CoinGecko (fallback) for crypto portfolio tracking.
- **Financial Screeners**: Automated fundamental analysis (ROE, debt, FCF, moat scoring) for equities.

## Alert Prioritization

Signals are classified into four tiers:

| Priority | Description | Response Time | Example |
|----------|-------------|---------------|---------|
| P1 - Critical | Market-moving events, security incidents | Immediate | Flash crash, major hack, regulatory ruling |
| P2 - High | Significant developments requiring attention | < 1 hour | Major product launch, earnings surprise, policy change |
| P3 - Normal | Noteworthy trends and updates | Daily digest | Research reports, industry analysis, funding rounds |
| P4 - Background | Context-building information | Weekly summary | Market commentary, opinion pieces, long-term trends |

## Escalation Workflow

```
Signal Detected
    │
    ├── P1: Immediate alert → Telegram DM to relevant team member
    │
    ├── P2: Queued for next check-in → included in briefing with highlight
    │
    ├── P3: Batched into daily digest → morning briefing (8AM)
    │
    └── P4: Archived for reference → weekly summary / knowledge base
```

### Escalation Rules
- **P1 signals** bypass all queues and are sent directly via Telegram
- **Duplicate signals** from multiple sources increase priority by one tier
- **Signals matching active portfolio positions** are automatically elevated
- **Contradictory signals** (e.g., bullish vs bearish on same asset) are flagged for human review

## Integration Points

### Team Collaboration
- **BotsHub (HXA-Connect)**: Agent-to-agent communication for coordinated signal analysis. Thread-based discussions allow multiple agents to contribute context.
- **Telegram Groups**: Real-time team communication for urgent signals and coordination.
- **GitHub**: Documentation and collaborative analysis stored in shared repos.

### Downstream Consumers
- **Daily Briefing**: Morning report aggregating top signals across all categories (AI/tech, finance, macro, research).
- **Portfolio Tracker**: Market data feeds into crypto and equity dashboards for visual monitoring.
- **Knowledge Base**: Validated insights extracted from signals are preserved for long-term reference.

### Feedback Loop
- Team members can flag false positives to improve filtering
- Engagement metrics on shared reports inform future prioritization
- Missed signals identified in retrospectives are used to expand collection sources

## Operational Notes

- Scraper batch runs take ~45 minutes for 136 accounts; schedule pre-scrape 1 hour before briefing
- CoinGecko rate limits aggressively (~10 req/min); prefer CoinPaprika for bulk data
- X syndication API allows ~10 requests per 2-minute window; use 15s delays between accounts
- All monitoring runs are idempotent — safe to re-run on failure without duplication
