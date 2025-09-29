# TSLA EMA/RSI — Negative Finding

**Question:** Do EMA crossover + RSI(14) filters produce tradable returns on TSLA (2012–2025)?

**Answer:** No.  
- After leak-free timing (next-open execution),  
- with costs (1 bps fees + 5 bps slippage),  
- and volatility targeting (10% ann vol, cap 1.5×),  

the edge fails out of sample. It only worked during the 2019–2021 bull market (VALID), but not in TRAIN or TEST.

## Key Results
- Train Sharpe: ~–0.40  
- Valid Sharpe: ~+0.86  
- Test Sharpe: ~–1.21  

**Conclusion:** Regime-specific overfit → no persistent edge.

## Files
- `tsla_ema_rsi_negative_finding.ipynb`: full code + plots  
