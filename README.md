# Volatility is Rough

An empirical replication of the foundational rough-volatility paper, using high-frequency realized-volatility data for the S&P 500 and ~30 other global equity indices.

> **Reference:** Gatheral, J., Jaisson, T. & Rosenbaum, M. (2018). *Volatility is Rough.* [arXiv:1410.3394](https://arxiv.org/pdf/1410.3394)


---

## Overview

Classical stochastic-volatility models (Heston, SABR, etc.) assume volatility is driven by a standard Brownian motion, which corresponds to a **Hurst exponent of H = 0.5**. The "rough volatility" literature shows this is empirically wrong: log-volatility behaves like a fractional Brownian motion with a Hurst exponent of roughly **H ≈ 0.1**, meaning volatility paths are far *rougher* (more jagged, with stronger short-term mean reversion) than a Brownian motion.


This project reproduces that result from scratch:

1. Estimates the Hurst exponent of realized volatility via the **scaling of moments** of log-volatility increments.
2. Cross-checks it with an independent **autocorrelation-based** estimator.
3. Contrasts the classical **FSV** model against the **Rough FSV (RFSV)** model.
4. Builds an **RFSV volatility forecaster** and benchmarks it against standard **AR** and **HAR** models.


## References

- Gatheral, J., Jaisson, T. & Rosenbaum, M. (2018). *Volatility is Rough.* [arXiv:1410.3394](https://arxiv.org/pdf/1410.3394)
- [Rough volatility — Wikipedia](https://en.wikipedia.org/wiki/Rough_volatility)
- [Hurst exponent — Wikipedia](https://en.wikipedia.org/wiki/Hurst_exponent)
- [Fractional Brownian motion — Wikipedia](https://en.wikipedia.org/wiki/Fractional_Brownian_motion)