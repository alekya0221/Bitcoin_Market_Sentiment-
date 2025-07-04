# Bitcoin_Market_Sentiment

#  Trading in the Mood:
## Analyzing Crypto Trader Behavior Through the Lens of Market Sentiment

---

###  Project Overview
This project investigates how market sentiment—quantified via the **Bitcoin Fear & Greed Index**—shapes the behavior and profitability of cryptocurrency traders. By blending **daily sentiment signals** with **historical trading data from Hyperliquid**, the analysis uncovers patterns in trading activity, risk-taking, and profit outcomes under various emotional market climates.

---

###  Objectives

- Understand whether trader activity increases during emotionally charged sentiment states (like "Extreme Fear" or "Extreme Greed")
- Examine how performance metrics such as total PnL, average PnL, and win-day frequency behave across sentiment classifications
- Identify whether **counter-sentiment strategies** (e.g., buying during Fear) correlate with improved outcomes
- Evaluate the role of sentiment as a **contextual factor** for strategy design and risk management

---

###  Data Sources

-  [Hyperliquid Trader Performance Dataset (daily metrics)](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)  
-  [Bitcoin Fear & Greed Index Data (sentiment labels)](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

Both datasets are merged by date to label each trading day with a sentiment classification. Preprocessing steps ensure missing values are handled, derived metrics (like profit-day flags) are computed, and `Unknown` sentiment rows are excluded from summaries.

---

### Key Components

- **Data Wrangling**: Merge trading data with sentiment, clean nulls, compute `daily_profit_day`
- **Descriptive Statistics**: Summary stats by sentiment class (mean, median, std across PnL/trade metrics)
- **Rolling Averages**: 3-day smoothed performance trends to reduce day-level noise
- **Visual Analysis**: Bar charts, line plots, box plots, and correlation matrices
- **Insight Generation**: Clearly defined strategic takeaways based on sentiment-performance patterns

---

### Key Findings

- **Fear & Extreme Fear** regimes yield higher average PnL and more profitable days, but also greater volatility
- **Greed-based markets** see higher activity but do not correlate with stronger returns
- **Neutral sentiment** is surprisingly stable and consistent—potentially favorable for algorithmic strategies
- **Sentiment is weakly correlated to profitability**, but slightly negatively correlated with trade count and volume

---

### Strategic Recommendations

- **Exploit Fear Responsibly**: Deploy carefully sized positions during fearful sentiment phases with stronger risk rules
- **Dial Back in Greed**: Avoid overexposure and FOMO-fueled trades when sentiment is overly optimistic
- **Sentiment as an Overlay**: Use sentiment as a decision-weighting factor, not a primary entry/exit trigger
- **Adjust Risk by Sentiment**: Tweak stop-losses and capital at risk depending on the volatility of the sentiment climate

---

### Limitations

- Daily-level resolution only (no per-trade granularity)
- Profit-day proxy used in absence of actual win/loss trades
- No macroeconomic news or external variables included in modeling
- Group-level patterns may not reflect individual trader behavior

---

### Future Enhancements

- Incorporate per-trade data to compute true win rates and risk-adjusted returns
- Model lagged sentiment effects (e.g., does Fear today predict performance tomorrow?)
- Segment traders into clusters and assess sentiment reactivity
- Bring in macro and technical overlays to enhance modeling accuracy

---

### Deliverables

- Clean Python notebook (.ipynb) with code, charts, and Insights
- Final merged dataset and filtered statistics summary
- Executive summary of insights
- Project_Summary_for_clients.pdf : Project Report: Trading in the Mood
A complete analysis of how crypto trader performance varies across market sentiment states (Fear, Greed, Neutral, etc.).

What’s Inside:
- Executive summary for clients and decision-makers
- Data sources, objectives, and analytical methodology
- Visual insights: box plots, heatmaps, rolling averages, and more
- Key takeaways on how sentiment influences behavior
- Strategic recommendations for sentiment-aware trading


---

> _“Sentiment doesn’t predict profits—but it does set the emotional stage. This project turns that stage into actionable strategy.”_
