# TSLA EMA/RSI — A Negative Finding

**Question:** Do EMA crossover + RSI(14) filters produce tradable returns on TSLA (2012–2025)?  
**Answer:** No. After leak-free timing, realistic costs, and volatility targeting, the edge fails out of sample. It only performs during the 2019–2021 bull run, and collapses before and after.  

---

## Equity Curve & Drawdown (Long-only, Vol Targeted)

![Equity Curve — Long-only (VT)](artifacts/long_only_vt_eq_dd.png)

- The strategy briefly compounds during the 2020–2021 bull market.  
- Outside that window, returns are flat to negative.  
- Drawdowns persist across other regimes, showing lack of robustness.  

---

## Monthly Returns Heatmap (Long-only, Vol Targeted)

![Monthly Heatmap — Long-only (VT)](artifacts/long_only_vt_monthly.png)

- Green = positive months, red = negative months.  
- Notice concentration of strong returns in 2020–2021.  
- Most other years show inconsistent or negative performance.  

---

## Rolling 6-Month Sharpe Ratio (126d)

![Rolling Sharpe — Long-only (VT)](artifacts/long_only_vt_rolling_sharpe.png)

- Sharpe ratio spikes > +3 during 2020–2021 (bull regime).  
- Collapses < –2 during sideways/volatile years like 2022–2023.  
- Confirms regime dependency → no persistent edge.  

---

## CSV Outputs
- [bt_long_only_vt.csv](artifacts/bt_long_only_vt.csv)  
- [bt_bull_only_vt.csv](artifacts/bt_bull_only_vt.csv)  
- [bt_longshort_vt.csv](artifacts/bt_longshort_vt.csv)  

---

## Conclusion

- **Train Sharpe:** ~ –0.40  
- **Valid Sharpe:** ~ +0.86  
- **Test Sharpe:** ~ –1.21  

👉 The edge is not robust — it overfits to a single bull regime.  
**This is a negative finding.** That in itself is valuable, as it demonstrates rigorous workflow: no look-ahead bias, proper splits, realistic costs, and volatility targeting.

---

## Personal Note

This was my **first backtest project** in my quant skill development journey.  
I worked through it with the help of GPT-5 using an *active learning* style: writing, running, and debugging code step by step until I reached a complete, reproducible result.  

The outcome (a negative finding) is part of the process — most strategies don’t survive out-of-sample.  
Publishing this helps me build disciplined habits and a transparent research track record.
