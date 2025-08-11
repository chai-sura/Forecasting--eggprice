# Forecasting Volatile Egg Prices for Procurement Planning

This project forecasts monthly U.S. egg prices to help **Mister Smith’s**, a bakery in Vermillion, SD, plan for cost volatility. In late 2024, a sudden price spike forced a $0.50 surcharge on egg-based dishes, leading to customer dissatisfaction and profit margin issues. By analyzing 30 years of historical data, the model provides actionable insights for pricing, procurement, and supplier negotiations.

---

## Business Problem
Egg prices are unpredictable, making it hard to maintain stable menu prices or negotiate with suppliers. Without a forecast, the bakery reacts to changes instead of planning ahead, risking customer trust and profitability.

---

## Key Questions
1. What will egg prices be over the next 12 months?  
2. When do seasonal price spikes occur?  
3. How big could price swings be?  
4. Can the forecast be trusted for budgeting?

---

## Data
- **Nominal Egg Prices** (BLS, 1995–2025)  
- **CPI for Eggs** (inflation-adjusted prices)  
Source: **FRED** API

---

## Approach
- Explored long-term trends, seasonal patterns, and volatility  
- Compared **Naïve**, **ETS**, and **ARIMA** models using rolling validation  
- Chose **ARIMA(4,0,0)(2,0,0)[12]** for best accuracy  
- Validated on unseen 2024 data

---

## Findings
- Prices consistently spike in **Nov–Jan**  
- Volatility has increased since 2020  
- ARIMA performed best but underpredicted sharp late-2024 jumps  

---

## Recommendations
1. Buy in bulk before winter to avoid seasonal peaks  
2. Use ~$3.40/dozen as a budget baseline  
3. Act on forecast bands ($2.30–$4.70) for purchasing and pricing decisions  
4. Make gradual price changes instead of sudden surcharges

---

## Limitations
- No external factors included (e.g., feed costs, disease outbreaks)  
- Assumes past patterns will continue

---

### Tech Stack
Python, Pandas, Statsmodels, Matplotlib, FRED API
