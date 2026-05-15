<div align="center">

# 🤖 Claude Portfolio Watchdog

**AI-powered 24/7 monitoring for your IBKR portfolio**

[Features](#features) · [Quick Start](#quick-start) · [Documentation](#documentation) · [Disclaimer](#disclaimer)

[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Built with Claude](https://img.shields.io/badge/Built%20with-Claude-orange.svg)](https://www.anthropic.com)

</div>

## What is this?

A complete AI analytics system that monitors your Interactive Brokers portfolio
24/7, detects critical signals, and generates Bloomberg-quality weekly reports.

Powered by Claude (Anthropic). Runs on GitHub Actions. Costs ~$1.50/month in API
fees — no SaaS subscription, no servers, no databases. All state is stored as
files inside your forked repository.

## Features

**Seven monitoring streams:**

- 🚨 Insider trading (SEC Form 4) — with cluster detection
- 📊 Analyst rating changes from major banks (Goldman, MS, JPM, …)
- ⚡ Significant price movements with S&P 500 context
- 📰 News filtered by Claude (1–10 importance score)
- 📅 Earnings calendar (3-day pre-warning + day-of)
- 🌐 Macro events (FOMC, CPI, PPI, NFP, GDP)
- 📈 Volatility & sector rotation (VIX, sector ETFs)

**Premium analytics:**

- Daily morning summary in Telegram
- Weekly 10–15 page PDF report (dark or light theme)
- Risk metrics — Beta, correlations, drawdowns, VaR
- Performance vs benchmark
- AI insights from Claude

## Quick Start

1. 📱 Create a Telegram bot via [@BotFather](https://t.me/BotFather) and grab the token.
2. 🔑 Get a [Claude API key](https://console.anthropic.com/) (~$5 covers 3–4 months).
3. 📋 **Use this template** to create your own private repo.
4. ⚙️ Edit `config.yaml` — set tickers, thresholds, schedule.
5. 🔐 Add three **GitHub Actions secrets**: `TELEGRAM_BOT_TOKEN`, `TELEGRAM_CHAT_ID`, `CLAUDE_API_KEY`.
6. 💼 Export your IBKR Position Report as CSV and drop it in `portfolio/`.
7. 🚀 Enable Actions in repository settings — the bot will run on its schedule.

**Total setup time: ~20 minutes.** Step-by-step guide with screenshots:
[INSTRUCTION.md](INSTRUCTION.md).

## Documentation

- 📘 [Full installation guide (RU)](INSTRUCTION.md)
- 🛠 [Troubleshooting](docs/TROUBLESHOOTING.md)
- 🔧 [Customization with Claude Code](docs/CUSTOMIZATION.md)
- 💰 [API costs breakdown](docs/API_COSTS.md)

## Disclaimer

This is **NOT investment advice**. All data is collected from public sources.
AI analysis is informational only and does not replace professional financial
counsel. All trading decisions remain entirely with the user.

## License

[MIT](LICENSE)
