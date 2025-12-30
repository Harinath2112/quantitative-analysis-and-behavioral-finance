Trader Behavior Insights: Bitcoin Market Sentiment vs. Hyperliquid Performance
📊 Project Overview
This project explores the relationship between Bitcoin Market Sentiment (Fear & Greed Index) and historical trader performance on the Hyperliquid exchange. The objective is to uncover hidden behavioral patterns and deliver data-driven insights to develop smarter trading strategies in the Web3 space.

This analysis was completed as part of the hiring process for the Junior Data Scientist role.

📁 Datasets Used
Bitcoin Market Sentiment Dataset: Daily classifications of market sentiment ranging from "Extreme Fear" to "Extreme Greed."

Hyperliquid Historical Trader Data: Detailed execution logs including account addresses, symbols, execution prices, sizes, sides (Buy/Sell), and closed PnL.

🚀 Key Technical Steps
Data Integration: Standardized disparate date formats (Unix/IST timestamps vs. ISO dates) to merge sentiment data with millions of individual trade executions.

Feature Engineering: Developed custom metrics such as Win_Rate (binary classification of PnL) and Avg_Trade_Size to quantify trader risk appetite.

Performance Mapping: Grouped trader success metrics across five sentiment categories to identify behavioral anomalies.

Side Analysis: Investigated the profitability of "Long" vs. "Short" positions relative to market mood.

💡 Core Insights
The Fear Premium: Data suggests that while trading volume often drops during "Fear" periods, the Average PnL per trade is higher, indicating that contrarian liquidity providers are better rewarded than momentum chasers.

Greed Trap: During "Extreme Greed," the Win Rate remains high (~46%), but the distribution of PnL shows a high risk of large-scale liquidations, likely due to increased leverage and overconfidence.

Behavioral Skew: Traders tend to over-trade (higher Trade_Count) during "Neutral" and "Greed" phases, often leading to higher cumulative fees that erode net profitability.

🧠 Proposed Strategy: Sentiment-Adjusted Scalping
Based on the analysis, I propose a Contrarian Momentum Strategy:

Mechanism: Dynamically scale position sizes based on the Fear & Greed Index.

Execution:

Extreme Fear (<25): Increase position size by 1.5x to capture the "Fear Premium" through limit orders.

Extreme Greed (>75): Reduce position size by 50% and cap leverage to 3x to protect against sudden market reversals.

Logic: This strategy exploits the mean-reversion behavior of the market while strictly managing the "fat-tail" risks identified during high-sentiment periods.

🛠️ Tech Stack
Language: Python

Libraries: Pandas, Seaborn, Matplotlib, NumPy

Environment: Jupyter Notebook / Google Colab
