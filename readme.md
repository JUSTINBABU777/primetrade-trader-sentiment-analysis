# Trader Performance vs Market Sentiment (Primetrade.ai)

## Overview
This project analyzes how market sentiment (Fear vs Greed) relates to trader behavior and performance on Hyperliquid. The objective is to uncover behavioral patterns and derive actionable insights that can inform risk-aware trading and strategy decisions.

The analysis focuses on understanding how traders adjust their activity, positioning, and outcomes under different sentiment regimes, and whether these effects vary across different trader segments.

---

## Datasets
This project uses two datasets:

1. **Bitcoin Fear & Greed Index**
   - File: `fear_greed_index.csv`
   - Contains daily Bitcoin market sentiment classifications (Fear, Greed, etc.) along with index values and dates.

2. **Hyperliquid Historical Trader Data**
   - File: `historical_data.csv`
   - Trade-level dataset including fields such as account, execution price, size, side (buy/sell), timestamp, and realized PnL.

---

## Methodology
The analysis follows these main steps:

1. **Data Quality Checks**
   - Verified dataset dimensions, missing values, and duplicates.
   - Both datasets were found to be clean and suitable for analysis.

2. **Data Preparation**
   - Converted Unix timestamps to datetime format.
   - Aggregated trade-level data to daily trader-level metrics.
   - Aligned trader performance with daily market sentiment.

3. **Sentiment vs Performance Analysis**
   - Compared daily PnL and win rate across Fear and Greed regimes.
   - Examined distributional differences to understand volatility and risk.

4. **Trader Behavior Analysis**
   - Analyzed changes in:
     - Trade frequency
     - Average trade size
     - Directional bias (long vs short)
   - Identified how trader behavior shifts under different sentiment conditions.

5. **Trader Segmentation**
   - Segmented traders based on:
     - Activity level (high vs low)
     - Risk proxy (high vs low)
     - Performance consistency (consistent vs inconsistent)
   - Evaluated how sentiment impacts each segment differently.

6. **Strategy Recommendations**
   - Derived actionable rules of thumb based on observed patterns.

---

## Key Insights
- Fear sentiment is associated with significantly higher trading activity and increased volatility.
- Average trade size remains relatively stable across sentiment regimes, indicating that risk is driven more by trading frequency than position sizing.
- Traders shift toward short positions during Fear, while Greed days show a more balanced directional bias.
- Consistent traders outperform across all sentiment regimes and demonstrate resilience during Fear markets.
- High-activity traders drive most of the performance swings and volatility.
- High risk-taking is not consistently rewarded, particularly during Greed conditions.

---

## Strategy Recommendations
- **Control trading frequency during Fear regimes:**  
  Since elevated risk during Fear is primarily driven by increased trading activity rather than larger position sizes, limiting excessive trade frequency—especially for high-activity traders—can help manage downside risk without materially reducing upside potential.

- **Prioritize consistent traders over aggressive risk-taking during Fear:**  
  Consistent traders perform well across all sentiment regimes and particularly during Fear conditions. Allocating capital toward consistent traders rather than increasing leverage or exposure improves resilience during volatile market phases.

---

## Limitations & Next Steps
This analysis is correlational and does not establish causality between sentiment and trader behavior. Leverage is approximated using available execution-related fields due to limited explicit leverage data. Additionally, daily aggregation may mask intraday behavioral dynamics.

Future work could incorporate explicit leverage and margin data, perform intraday sentiment alignment, apply clustering techniques to identify behavioral archetypes, or develop a lightweight dashboard for interactive exploration.

---

## How to Run
1. Clone this repository.
2. Ensure `fear_greed_index.csv` and `historical_data.csv` are present in the project directory.
3. Install required Python dependencies.
4. Open the notebook in the `notebooks/` folder.
5. Run the notebook from top to bottom to reproduce the analysis.

---

## Author
Justin Babu



