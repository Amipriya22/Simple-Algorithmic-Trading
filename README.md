# Simple Algorithmic Trading: Intraday Strategy Optimization

This project focuses on developing an intraday trading strategy for selected stocks by analyzing variations in their **Open**, **High**, **Low**, and **Close** prices. The goal is to identify optimal entry and exit times to maximize returns.

---

## Strategy Overview

We evaluate price movements using multiple threshold levels:

### Threshold Levels
- **k = 0.35%**
- **k = 0.5%**
- **k = 1%**
- **k = 2%**
- **k = 3.5%**

For each threshold \( k \), we:
- Count the number of times a stock’s **Open** or **High** price exceeds the threshold.
- Track these occurrences across different weeks.
- Multiply the counts by predefined weights to compute:
  - `P035`, `P05`, `P1`, `P2`, `P35`

---

## Time-Based Optimization

- We identify the **worst time** for each stock — the time after which it **never crosses** the threshold \( k \).
- Using this insight, we optimize:
  - **Entry time**: When to buy the stock
  - **Exit time**: When to sell the stock

This helps in designing a robust intraday strategy tailored to each stock’s behavior.

---

## Repository Contents
- `Data`: Dataset used for strategy testing
- `The Algorithm`: Python notebooks implementing the logic
- `README.md`: Project documentation

---

## Future Enhancements
- Incorporate volume and volatility metrics
- Extend strategy to multi-day swing trades
- Add backtesting and performance visualization

---

Feel free to fork, contribute, or reach out with suggestions!
