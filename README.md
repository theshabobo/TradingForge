# TradingForge v1.1.0

**Professional crypto trading automation for Windows. Single executable, no installation required.**

---

## Download

Download `TradingForge.exe` from the [Releases](../../releases) page.

---

## What's New in v1.1.0

- **Signals** — Connect TradingView alerts, custom scripts, or any webhook source to trigger real-time buy, sell, DCA, stop-loss, and take-profit actions on your running bot
- **Signal & Hybrid Modes** — Full automation mode or use signals as a gate alongside your own entry logic
- **Provider Management** — Define trusted providers and restrict which actions and pairs each one can affect
- **180-Day Signal Log** — Every signal received is logged with full status and rejection reasons
- **Bug Fix** — Resolved exe icon corruption that caused the window to open and immediately close on some systems

---

## Requirements

- Windows 10 or Windows 11 (64-bit)
- No installation, no Node.js, no dependencies

---

## Quick Start

1. Download `TradingForge.exe`
2. Place it in a folder of your choice (e.g. `C:\TradingForge\`)
3. Double-click to run — a console window will appear and stay open
4. Open your browser and go to `http://localhost:8081`
5. Log in and activate your license under **Settings → Server**

On first launch, TradingForge will extract its configuration files into the same folder as the exe. Do not move the exe after first run without also moving the extracted files.

---

## Features

### Trading Engines
- **TradeFuel** — DCA (Dollar Cost Averaging) engine with configurable safety orders, take-profit targets, and deviation step scaling
- **TradeSmith** — Indicator-based engine with EMA, RSI, MACD, and customizable pair filtering

### Signals
- Receive trade signals from any webhook source (TradingView, custom scripts, etc.)
- 9 supported actions: `buy`, `sell`, `cancel`, `close_all`, `dca`, `set_stop_loss`, `set_take_profit`, `pause`, `resume`
- Connects via a secure global relay — no port-forwarding required
- Configure from **Settings → Signals**

### Dashboard
- Real-time portfolio valuation in BTC and USD
- Live P&L tracking (daily, weekly, all-time)
- Active pair monitoring with DCA levels and position status
- Full trade history with buy/sell logs

### Risk Management
- Stop-loss and take-profit configuration per pair
- Paper trading mode (full simulation with virtual funds)
- Multiple strategy configuration profiles
- Hot-reload config without restarting

### Notifications
- Telegram bot integration
- Email alerts
- Trade execution, status, and error notifications

### Exchange Support
Binance · Coinbase Advanced · Bybit · Kraken · KuCoin · MEXC · Crypto.com · Gate.io · Gemini · Bitstamp

---

## Signals Setup (v1.1.0)

1. Activate your license — a signal token is generated automatically
2. Go to **Settings → Signals** and enable Signals
3. Copy your Webhook URL
4. Paste it into your TradingView alert or signal source as the webhook URL
5. Send a JSON payload:

```json
{
  "action": "buy",
  "pair": "BTCUSDT",
  "provider": "tradingview"
}
```

Full documentation: [tradingforge.net/wiki/signals/overview](https://tradingforge.net/wiki/signals/overview)

---

## License

TradingForge requires a paid perpetual license. One-time purchase, lifetime access, all features included.

Purchase at [tradingforge.net/buy](https://tradingforge.net/buy)

---

## Support & Documentation

- **Wiki:** [tradingforge.net/wiki](https://tradingforge.net/wiki)
- **Contact:** [tradingforge.net/contact](https://tradingforge.net/contact)
- **Community:** [r/TradingForge](https://www.reddit.com/r/TradingForge/)

---

## Security

- Never share your `.env` file or API keys
- Your webhook URL acts as a password — regenerate it from Settings if compromised
- TradingForge does **not** require withdrawal permissions on exchange API keys — use read + trade only

---

*TradingForge is not financial advice. Trading involves risk. Past performance does not guarantee future results.*
