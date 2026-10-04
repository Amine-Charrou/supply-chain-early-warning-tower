# Supply Chain Early-Warning Tower

> Forecast demand and flag stockouts and late deliveries before they happen.

![status](https://img.shields.io/badge/status-design%20stage-lightgrey) ![sprint](https://img.shields.io/badge/sprint-Weeks%2013--14-blue) ![project](https://img.shields.io/badge/portfolio-07%2F08-0891b2)

| | |
|---|---|
| **Category** | Forecasting & Operations Analytics |
| **Domain** | Logistics / Manufacturing |
| **Stack** | Python · statsmodels / Prophet · LightGBM · Power BI |
| **Status** | 🚧 Scoped — implementation not started |

## Overview

An operational analytics system that combines demand forecasting with two risk models: stockout in the next 7 days and late delivery. Alerts feed an executive control-tower dashboard covering inventory health, logistics and forecast accuracy.

## Business problem

Supply-chain managers need to anticipate demand shifts, stockouts, late deliveries and supplier issues before they hit operations.

## What this project demonstrates

- Time-series forecasting with rigorous backtesting
- Operational risk modelling
- Cost-aware alert design
- Turning analytics into an operational decision system

## Key points

- Forecast ladder: moving average → exponential smoothing → ARIMA / Prophet → gradient boosting
- Proper time-series validation (rolling-origin backtests, no leakage)
- Stockout-risk model (7-day horizon) and late-delivery risk model
- Rule-based alerts with thresholds tied to the cost of a stockout vs. overstock
- Dashboard: inventory health, days of stock, supplier performance, actual vs. forecast
- KPIs: forecast accuracy, stockout rate, on-time delivery, inventory turnover

## Planned architecture

```text
Orders, inventory, suppliers, shipments
   ↓
Demand forecasting (baseline → advanced)
   ↓
Stockout-risk (7-day) & late-delivery models
   ↓
Cost-based alert rules
   ↓
Control-tower dashboard
```

## Planned deliverables

- [ ] Forecasting pipeline with rolling backtests
- [ ] Stockout and delivery risk models
- [ ] Alert logic
- [ ] Power BI control tower (overview, inventory, logistics, forecast)
- [ ] Business recommendations

## Success metrics

- Forecast accuracy (MAPE / WAPE)
- Stockout rate, on-time delivery, late-shipment rate
- Inventory turnover and days of inventory

## Planned structure

```text
data/  notebooks/  src/{forecasting,risk,alerts}  dashboard/  docs/
```

## Roadmap

- [x] Scope and README
- [ ] Data collection / generation
- [ ] Core implementation
- [ ] Evaluation and business-impact estimate
- [ ] Demo, write-up and interview notes

---

Part of my **Data & AI × Business Consulting** portfolio, a 16-week sprint of 8 projects going from data and BI to ML, GenAI, agents, automation and AI strategy. See all projects on my [GitHub profile](https://github.com/Amine-Charrou).

*Amine Charrou · Final-year Data Science & AI engineering student, ENSA Agadir · [LinkedIn](https://www.linkedin.com/in/amine-charrou/)*
