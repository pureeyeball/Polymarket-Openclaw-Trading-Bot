<div align="center">

# 🐾 OpenClaw — Polymarket Trading Bot

**A fast, beginner-friendly automated trading bot for [Polymarket](https://polymarket.com)**

<br/>

![Downloads](https://img.shields.io/badge/downloads-20k%2B-brightgreen?style=for-the-badge&logo=github)
![Stars](https://img.shields.io/github/stars/yourusername/openclaw-polymarket-bot?style=for-the-badge&color=yellow&logo=github)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/status-active-success?style=for-the-badge)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-ff69b4?style=for-the-badge)

<br/>

[**🚀 Quick Start**](#-quick-start) · [**✨ Features**](#-features) · [**⚙️ Setup**](#️-setup) · [**📖 Docs**](#-configuration) · [**🤝 Contributing**](#-contributing)

</div>

---

## 📌 About

**OpenClaw** is an open-source trading bot built for **Polymarket**, the leading prediction market platform. It watches markets, applies configurable strategies, and executes trades automatically — so you can trade smarter without staring at charts all day.

Trusted by **20,000+** downloads and growing. 🎉

> ⚠️ **Disclaimer:** Trading involves risk. This tool is provided as-is for educational and research purposes. Always test with small amounts first, and never trade money you can't afford to lose.

---

## ✨ Features

| | |
|---|---|
| 🤖 **Automated Trading** | Set rules once, let the bot handle execution 24/7 |
| 📊 **Strategy Engine** | Plug in custom or prebuilt strategies (momentum, arbitrage, mean-reversion) |
| 🔔 **Real-Time Alerts** | Get notified via Discord/Telegram when trades trigger |
| 🛡️ **Risk Management** | Built-in stop-loss, position sizing, and exposure limits |
| 📈 **Backtesting** | Test strategies against historical market data before going live |
| 🧩 **Modular Design** | Easily extend with your own modules and data sources |
| 🖥️ **Simple CLI & Config** | No coding required to get started — just edit a config file |
| 🔑 **Secure by Default** | API keys stay local, never leave your machine |

---

## 🚀 Quick Start

Get up and running in under 5 minutes:

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/openclaw-polymarket-bot.git
cd openclaw-polymarket-bot

# 2. Install dependencies
pip install -r requirements.txt

# 3. Copy the example config
cp config.example.yaml config.yaml

# 4. Add your Polymarket API credentials to config.yaml

# 5. Run the bot 🎉
python run.py
```

---

## ⚙️ Setup

### 1️⃣ Prerequisites

- 🐍 Python 3.10 or higher
- 🔑 A Polymarket account with API access enabled
- 💼 A crypto wallet (e.g., MetaMask) funded on Polygon for trading

### 2️⃣ Installation

```bash
git clone https://github.com/yourusername/openclaw-polymarket-bot.git
cd openclaw-polymarket-bot
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3️⃣ Configuration

Rename `config.example.yaml` to `config.yaml` and fill in your details:

```yaml
polymarket:
  api_key: "YOUR_API_KEY"
  wallet_address: "YOUR_WALLET_ADDRESS"
  private_key: "YOUR_PRIVATE_KEY"   # ⚠️ keep this secret, use env vars in production

strategy:
  name: "momentum"
  max_position_size: 100      # in USDC
  stop_loss_percent: 5

notifications:
  discord_webhook: "YOUR_WEBHOOK_URL"
```

> 💡 **Tip:** Never commit `config.yaml` or your private key to version control. Use a `.env` file or secret manager for production deployments.

### 4️⃣ Run It

```bash
python run.py
```

You should see live logs of the bot scanning markets and (optionally) placing trades:

```
[INFO] Connected to Polymarket ✅
[INFO] Scanning 128 active markets...
[INFO] Signal found: "Will X happen by Y?" → BUY YES @ 0.62
[INFO] Order placed successfully 🎯
```

---

## 🧠 Choosing a Strategy

| Strategy | Best For | Risk Level |
|---|---|---|
| 🐢 `mean-reversion` | Stable, range-bound markets | 🟢 Low |
| 🚀 `momentum` | Trending, high-volume markets | 🟡 Medium |
| ⚡ `arbitrage` | Cross-market price gaps | 🔴 High |

Swap strategies anytime in `config.yaml` under `strategy.name`.

---

## 🧪 Backtesting

Before going live, test your strategy against historical data:

```bash
python backtest.py --strategy momentum --start 2025-01-01 --end 2025-06-01
```

This outputs a performance report with win rate, P&L, and drawdown charts.

---

## 🗂️ Project Structure

```
openclaw-polymarket-bot/
├── run.py                 # Entry point
├── backtest.py            # Backtesting engine
├── config.example.yaml    # Example configuration
├── strategies/             # Built-in & custom strategies
├── core/                   # Trading engine, order management
├── notifications/          # Discord/Telegram integrations
└── tests/                  # Unit tests
```

---

## 🤝 Contributing

Contributions are welcome and appreciated! 💛

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing-idea`)
3. Commit your changes (`git commit -m 'Add amazing idea'`)
4. Push to the branch (`git push origin feature/amazing-idea`)
5. Open a Pull Request

Check out [`CONTRIBUTING.md`](CONTRIBUTING.md) for guidelines.

---

## 📜 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

<div align="center">

### ⭐ If OpenClaw helps you trade smarter, consider giving it a star!

Made with ❤️ by the OpenClaw community

</div>
