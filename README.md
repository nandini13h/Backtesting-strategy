Moving Average Crossover Strategy with Volume Confirmation

Overview

This project implements a rule-based trading strategy on **State Bank of India (SBIN.NS)** using Python. The objective is to evaluate whether a moving average crossover system combined with volume confirmation can generate profitable trading signals.
The strategy was backtested on historical market data from January 2020 to January 2024 using the Yahoo Finance API.


Strategy Logic

Buy Signal
 A long position is opened when:
 20-Day Simple Moving Average (SMA20) crosses above the 50-Day Simple Moving Average (SMA50)
 Daily trading volume is greater than the 20-Day Average Volume

Sell Signal
 A position is closed when: SMA20 crosses below SMA50
 Only one position can be held at a time.



Data Source

* Yahoo Finance
* Ticker: SBIN.NS
* Time Period: 2020-01-01 to 2024-01-01


Tools & Libraries
Python, Pandas, yFinance, Matplotlib


Backtesting Assumptions

Initial Capital: ₹100,000
Full capital invested on each buy signal
No leverage
No transaction costs or slippage
Long-only strategy


Performance Results

| Metric                | Value       |
| --------------------- | ----------- |
| Initial Capital       | ₹100,000    |
| Final Portfolio Value | ₹154,057.59 |
| Net Profit            | ₹54,057.59  |
| Strategy Return       | 54.06%      |
| Buy & Hold Return     | 100.59%     |
| Sharpe Ratio          | 0.71        |
| Maximum Drawdown      | -24.12%     |


Analysis

The strategy generated a positive return of 54.06% over the testing period, demonstrating that trend-following signals were able to capture a portion of SBI's upward movement.
However, the strategy underperformed a simple buy-and-hold approach, which returned **100.59%** during the same period.

Possible reasons include:
Delayed entry and exit caused by moving average lag
Missed gains during strong trending periods
Whipsaw trades during sideways market conditions
Volume confirmation filtering out some profitable signals

Despite lower absolute returns, the strategy provides a systematic framework for trend detection and risk management.

