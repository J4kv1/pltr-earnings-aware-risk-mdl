# pltr-earnings-aware-risk-mdl
Earnings aware Monte Carlo RM for Palantir Technologies that compares baseline and event driven VaR and CVaR around the Feb 2, 2026 earnings announcement.


 ------ Earnings Aware Monte Carlo Risk Model (PLTR)

Overview

I created a piece that analyzes Palantir Technologies’ short horizon downside risk using Monte Carlo (MC) simulation. A baseline risk model is compared against an earnings aware extension that explicitly incorporates jump risk from the February 2, 2026 earnings announcement.

The goal is to quantify how much tail risk is underestimated when discrete earnings events are ignored.

Methodology

* Historical daily log returns are estimated from PLTR price data.
* A baseline Monte Carlo model assumes a single normal return distribution derived from non earnings trading days.
* An earnings aware model treats earnings day returns separately to capture event driven volatility.
* Simulated price paths are generated for both models.
* Downside risk is evaluated using 95 percent Value at Risk (VaR) and Conditional Value at Risk (CVaR) on a $10,000 position.

Findings

* Earnings aware VaR and CVaR are materially higher than baseline estimates.
* Ignoring earnings events leads to systematic underestimation of tail risk.
* A disproportionate share of PLTR’s downside risk is concentrated around earnings announcements.

Tools

* Python
* OpenAI
* NumPy
* pandas
* yfinance
* matplotlib

Notes

Not actual price prediction. The model is intended for educational and analytical purposes and DOESN'T constitute investment advice.
