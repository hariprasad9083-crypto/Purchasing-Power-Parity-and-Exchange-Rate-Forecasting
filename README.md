# Purchasing Power Parity & Exchange Rate Forecasting

Testing whether Purchasing Power Parity (PPP) theory holds for the USD/CAD
exchange rate, then building a time-series model to forecast it.

## Overview

PPP theory says exchange rates should move with inflation differentials between
two countries. This project tests that claim on real USD/CAD data, then forecasts
the rate using ARIMA modelling.

**Key finding:** inflation differentials explained only ⟨~18%⟩ of exchange rate
movement — PPP alone is a weak predictor, so a time-series approach was used
for forecasting.

## Data

- **Pair:** USD/CAD exchange rate
- **Period:** ⟨2010–2021, monthly⟩
- **Sources:** ⟨exchange rate + US CPI + Canada CPI⟩

## Methodology

1. **Exploratory analysis** — indexed comparison of US CPI, Canada CPI, and USD/CAD
2. **Stationarity testing** — Augmented Dickey-Fuller (ADF) tests; differencing applied
3. **PPP evaluation** — tested inflation differential against exchange rate movement
4. **Model selection** — compared 6 ARIMA specifications by AIC/BIC and coefficient significance
5. **Forecasting** — best model ⟨ARIMA(2,1,0)⟩ used to forecast 2021 values with 95% confidence intervals

## Tools

Python · pandas · statsmodels · matplotlib

## Results

- ADF tests confirmed stationarity of series after first differencing
- Best model: ⟨ARIMA(2,1,0)⟩ (lowest AIC, all coefficients significant)
- Produced 12-month 2021 forecast of ln(USD/CAD) with 95% CI bands

## Author

Hariprasad Yogaraju — ⟨www.linkedin.com/in/hari-prasadin⟩
