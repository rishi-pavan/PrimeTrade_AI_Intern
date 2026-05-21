# PrimeTrade AI: Market Sentiment & Trade Execution Analysis

PrimeTrade AI is a data analysis project designed to explore relationships between historical cryptocurrency trade executions and macro market sentiments. By merging transactional ledger histories with historical Crypto Fear & Greed index values, this project attempts to uncover how retail or institutional trading behavior correlates with shifting psychological trends in the market.

## 🚀 Overview

The primary notebook (`primetrade_ai.ipynb`) performs extensive exploratory data analysis (EDA), cleaning, and visualization on transaction data spanning various crypto assets (such as FARTCOIN and other mapped assets) to track metrics like PnL distribution, trading velocity, and order sizes under differing sentiment conditions.

### Key Insights Discovered
* **Extreme Fear:** Market participants display strong tendencies toward bargain-hunting, leading to higher overall buying frequencies when asset prices decline.
* **Fear & Greed Phases:** Profit-taking behaviors take priority; cautious selling marginally outweighs buying as traders de-risk or secure gains.
* **Neutral Market:** Trading activity scales down to a heavily balanced equilibrium between buy and sell orders.
* **Extreme Greed:** High market velocity and intense participation, with both buying and selling volume surging due to maximum confidence and liquidity deployment.

---

## 📊 Dataset Structure

The notebook is built to process two essential data streams:

1. **`historical_data.csv`**: Contains fine-grained transaction history parameters including:
   * `Account`, `Coin`, `Execution Price`, `Size Tokens`, and `Size USD`
   * Order properties: `Side` (BUY/SELL), `Direction` (e.g., Close Long), and `Closed PnL`
   * Blockchain properties: `Transaction Hash`, `Order ID`, `Fee`, and Unix `Timestamp` strings.
2. **`fear_greed_index.csv`**: Contains macro market tracking statistics:
   * `timestamp`, `value` (0-100 score), and `classification` (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
