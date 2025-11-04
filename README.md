# Public Transport Passenger Forecasting Report


---

## Dataset Summary
- **Data Range:** 2019 - 2024  
- **Frequency:** Daily  
- **Attributes:** Date, Local Route, Light Rail, Peak Service, Rapid Route, School, Other

The dataset was cleaned, sorted by date, and missing values were removed before performing analysis and forecasting.

---

## Key Insights
1. The service type with the **highest average passengers** is **'Rapid Route'**, averaging **12,630 passengers per day**.
2. **'Rapid Route'** shows the **highest volatility**, indicating irregular passenger patterns across the observed timeline.
3. **'School'** services display the **highest growth rate**.
4. The **strongest correlation (0.97)** exists between **'Light Rail'** and **'Rapid Route'**, suggesting shared demand patterns and possible operational interdependence.

---

## Forecasting Approach

### Model Used: ARIMA (AutoRegressive Integrated Moving Average)
- The ARIMA model was chosen for short-term forecasting of passenger journeys for **Local Route**, **Light Rail**, and **Peak Service**.  
- Model Order: **(2, 1, 2)**  
- Forecast Horizon: **5 Days** 

---

## 5-Day Forecast Results

| Forecast Date | Local Route | Light Rail | Peak Service |
|----------------|-------------|-------------|--------------|
| 2024-09-24 | 10930.30 | 7911.64 | 212.36 |
| 2024-09-25 | 16243.40 | 10331.47 | 336.01 |
| 2024-09-26 | 13399.76 | 8262.60 | 300.22 |
| 2024-09-27 | 6130.85 | 4104.11 | 160.39 |
| 2024-09-28 | 519.36 | 1204.69 | 35.10 |

---

## Model Evaluation

### Evaluation Metrics

| Metric | Local Route | Light Rail | Peak Service |
|:--|--:|--:|--:|
| **MAE** | 6179.45 | 4020.90 | 103.70 |
| **MSE** | 54,153,214.54 | 23,575,773.86 | 15,399.84 |
| **RMSE** | 7,358.89 | 4,855.49 | 124.10 |
| **MAPE** | 12,194.48% | 350.08% | ∞ |
