<div align="center">

# Polymarket OpenClaw Trading Bot

A self-hosted, automated trading bot for prediction markets on [Polymarket](https://polymarket.com)

![Downloads](https://img.shields.io/badge/downloads-23k%2B-brightgreen?style=for-the-badge&logo=github)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/python-3.13-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/status-active-success?style=for-the-badge)
![Rating](https://img.shields.io/badge/rating-4.5%2F5_%E2%98%85-yellow?style=for-the-badge)

[Features](#features) · [Download](#download) · [Installation](#installation) · [FAQ](#faq)

</div>

---

## About

OpenClaw is a self-hosted trading bot for **Polymarket**, the largest prediction market platform. It runs entirely on your own machine, connects directly to your wallet and the Polymarket API, and executes trades automatically based on rules and strategies you configure — no cloud service, no middleman, no data leaving your system.

It's built for traders who want to automate positions on prediction markets (elections, sports, crypto prices, current events, etc.) without manually watching order books all day.

> Trading involves risk. This tool is provided as-is for educational and research purposes. Test with small amounts before running it unattended.

## Features

- **Self-hosted** — runs locally, your API keys and private keys never leave your machine
- **YES/NO market trading** — places and manages orders on Polymarket's binary outcome shares automatically
- **Automated execution** — define rules once, the bot trades 24/7 across active markets without manual input
- **Strategy engine** — built-in strategies (momentum, mean-reversion, order book arbitrage) tuned for prediction market price behavior
- **Odds & probability tracking** — monitors implied probability shifts as markets move toward resolution
- **Category filtering** — target specific market categories (elections, sports, crypto, economics, current events)
- **Risk management** — stop-loss, position sizing, and exposure limits configurable per strategy or per market
- **Resolution-aware exits** — automatically reduces or closes positions as a market approaches its resolution date
- **Backtesting** — validate a strategy against historical Polymarket price and volume data before going live
- **Notifications** — optional Discord/Telegram alerts on order fills and market resolutions
- **USDC-native** — trades directly in USDC, matching Polymarket's settlement currency

## Download

Latest release: **23,000+ downloads**

Get the latest version from the [Releases](https://github.com/yourusername/openclaw-polymarket-bot/releases) page.

## Installation

Download the latest release from the [Releases](https://github.com/yourusername/openclaw-polymarket-bot/releases) page, then:

```bash
cd openclaw-polymarket-bot
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip install -r requirements.txt
python run.py
```

**Requirements**
- Python 3.13
- A Polymarket account with API access enabled
- A funded wallet on Polygon (for placing trades)

## FAQ

**Is this hosted for me, or do I run it myself?**
OpenClaw is fully self-hosted. You run it on your own machine or server — nothing is processed on external infrastructure.

**Which markets does it trade?**
Any market listed on Polymarket that your configured strategy targets — elections, sports, economic events, crypto prices, and more.

**Is my private key safe?**
Your private key stays local and is never transmitted anywhere except directly to the blockchain when signing transactions.

**Do I need to know how to code?**
No. Configuration is straightforward. Writing custom strategies requires Python, but it's optional.

**Can I test before trading real funds?**
Yes — use the built-in backtester against historical data, or point the bot at a small test position size first.

**What Python version is required?**
Python 3.13.

## License

MIT — see [LICENSE](LICENSE) for details.
