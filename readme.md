# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes how market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid. The objective is to identify behavioral patterns and actionable insights that can inform risk-aware trading strategies.

## Datasets
- Bitcoin Fear & Greed Index (daily sentiment)
- Hyperliquid historical trader data (trade-level)

## Methodology
- Cleaned and validated raw datasets
- Converted Unix timestamps and aggregated trade-level data to daily trader-level metrics
- Aligned trader outcomes with daily sentiment
- Analyzed performance differences across sentiment regimes
- Segmented traders by activity, risk proxy, and performance consistency

## Key Insights
- Fear regimes are associated with significantly higher trading activity and volatility
- Average trade size remains stable across sentiment regimes
- Consistent traders outperform across all sentiment conditions
- High-activity traders drive most performance swings

## Strategy Recommendations
- Reduce excessive trading frequency during Fear regimes
- Prioritize consistent traders over aggressive risk-taking during volatile periods

## How to Run
1. Install dependencies from `requirements.txt`
2. Open the notebook in the `notebooks/` folder
3. Run cells from top to bottom


