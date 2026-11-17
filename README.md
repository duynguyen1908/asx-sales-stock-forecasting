# Do Sales Explain Future Stock Prices?

*Individual project · University of Adelaide · Sep 2026*

**Question:** Can a company's sales predict its share price a year later?

**What I did**
- Cleaned and matched financial and price data for 25,451 ASX firm-years
- Tested the sales–price link with regression, adding controls step by step
- Forecast sales for three ASX companies and checked each forecast against a held-out year
- Built a Tableau dashboard of share prices across Australia

**Methods**
- **Data wrangling:** de-duplication with an anomaly log, per-share variables, winsorising, and a 12-month-ahead target with no look-ahead
- **Regression:** 4 nested models (OLS → fundamentals → industry/year effects → firm fixed effects), compared with adj. R², AIC and BIC
- **Diagnostics:** Breusch-Pagan → HC1 robust standard errors; VIF; residual plots; a sensitivity check on the sales transform
- **Forecasting:** ADF stationarity tests and ARIMA order selection, with the **final year held out from every modelling decision**; compared against a naive benchmark
- **Simulation:** 10,000-scenario Monte Carlo on log sales growth, with Shapiro-Wilk tests of the normality assumption

**Result:** Sales look like a strong signal on their own, but the effect **disappears** once company fundamentals are considered. Sales-based price forecasts are useful as ranges, not targets.

**Tools:** Python (pandas, statsmodels) · Tableau

📊 **[View the interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/duy.nguyen8153/viz/Predictive-ASXStockPricesAnalysis/ASXPriceStory)**

---
📂 **Full notes, code and results are available on request.** Message me on [LinkedIn](https://www.linkedin.com/in/duynguyen1908/) and I can share access to the private project repo.
