Hi everyone — I'm Lydia Xu.

This is my first meaningful quantitative finance project, where I apply the Fama-French factor model to stock selection. It’s a simple but practical strategy designed for beginners, demonstrating how to transform financial theory into a real, backtestable framework.

I learned a lot through this process — from designing the signal to evaluating performance — with helpful guidance from ChatGPT throughout. I hope this project can also inspire others who are starting their journey in quantitative investing.

Let’s keep making progress together 🚀


# 📈 Multi-Factor Alpha Strategy on S&P 100

This project implements a rolling IC-weighted multi-factor stock selection strategy on a subset of the S&P 100 index.

## Aim
 

## 📌 Strategy Overview

- **Universe**: 20 large-cap U.S. stocks (subset of S&P 100)
- **Factors Used**:
  - Momentum (12-1 month)
  - Gross Margin (real financial factor)
  - ROE (return on equity)
  - EPS growth
  - B/M ratio
This is a classic Fama-French + Quality + Growth stretagy 

- **Weighting**: Factors are standardized and combined using IC-based weights
- **Portfolio Construction**: Top 10 stocks by score, weighted using Softmax
- **Rebalancing**: Every 21 trading days
- **Benchmark**: SPY

## 🔍 Highlights
Original
facotrs: roe + bm + EPS + momentum 
- IC-weighted factor scores dynamically reflect predictive power
- Rolling backtest with realistic constraints
- Performance Summary:
  - Annual Return: ~36.8%
  - Sharpe Ratio: ~1.99
  - Max Drawdown: ~12.9%
Looking from the IC timeline, notice BM factor maybe inefficient, Sharpe Ratio may indicate overfitting

Updrading
facotrs: roe + gross margin + EPS + momentum
- add Softmax weighting emphasizes higher-scoring stocks
- Performance Summary:
  - Annual Return: ~39.3%
  - Sharpe Ratio: ~1.96
  - Max Drawdown: ~15.10%

### 📈 Does the Strategy Generate True Alpha? (remaining question)

To evaluate whether the strategy's performance is driven by genuine alpha (stock selection skill) or simply market exposure (beta), we compare its returns with SPY:

- The strategy consistently outperforms SPY in cumulative return
- It has a higher Sharpe Ratio and lower drawdown
- This suggests positive alpha, not just beta-driven performance

* In future work, formal factor regressions (e.g., against Fama-French 3/5 factors) could be used to isolate and validate alpha generation.

  
## 📁 Project Structure

```
multi-factor-alpha-strategy/
├── alpha_strategy.ipynb         # Main notebook
├── gross_margin.csv             # Real gross margin data (scraped)
├── fundamentals.csv             # Optional financials data
├── requirements.txt             # Python dependencies
├── README.md                    # Project documentation
```
## 🚀 How to Use

```bash
pip install -r requirements.txt
jupyter notebook alpha_strategy.ipynb
```

## 🧠 Author

Lydia Xu | Quantitative Finance Student @ University of Waterloo
