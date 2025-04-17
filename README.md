# CryptoTradingData
# 🤖 Build AI Crypto Agents with altFINS Data API

The [altFINS Crypto Market & Analytical Data API](https://altfins.com/crypto-market-and-analytical-data-api/) is the perfect data source for powering AI agents, LLM-based tools, and GPT-driven crypto analysis. It provides:

- Real-time and historical market data
- 120+ technical indicators (RSI, MACD, Bollinger Bands, etc.)
- 33 candlestick patterns
- Coverage of 3,000+ coins
- Multiple timeframes: 15m, 1h, 4h, 12h, 1d

Ideal for:
- 🧠 AI agents and copilots
- 🤖 LangChain / Autogen-powered trading assistants
- 📊 Market scan and signal automation
- 🛠️ Backtesting and quant tools

---

## 🏁 Quick Start (Python)
```bash
pip install requests
```

```python
import requests

API_KEY = "YOUR_API_KEY"
headers = {"Authorization": f"Bearer {API_KEY}"}

url = "https://api.altfins.com/v1/assets/analytics"
params = {
    "interval": "1d",
    "limit": 5
}

response = requests.get(url, headers=headers, params=params)
data = response.json()

for asset in data.get("data", []):
    print(asset["symbol"], asset["technicalIndicators"].get("rsi"))
```

---

## 🤖 Build an AI Agent with GPT-4
Use altFINS data to power LLMs with real-time market intelligence.

```python
from openai import OpenAI

prompt = f"""
You are a crypto analyst.
Here is daily market data for several coins:
{data}

Which coin shows the strongest bullish momentum? Why?
"""

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[{"role": "user", "content": prompt}]
)

print(response.choices[0].message.content)
```

---

## 🔁 Example AI Agent Use Cases
- 🔍 Scan altFINS data for coins matching bullish signals → GPT generates trade rationale
- 📉 Feed altFINS patterns into a LangChain agent that outputs technical summaries
- 🧪 Use in Autogen multi-agent systems for strategy simulation or portfolio rebalancing

---

## 🧪 Try the Demo
Sign up for [demo access here](https://altfins.com/crypto-market-and-analytical-data-api/) to get your API key and test it live.

---

## 📚 Learn More
- [Full API documentation](https://altfins.com/crypto-market-and-analytical-data-api/)
- [altFINS homepage](https://altfins.com)

---

## 🙌 Contributing
Have ideas or want to show off what you’ve built with the API? Open a pull request or issue!
