# City of Manila Seasonal Weather Forecasting: A Comparative Study
### Evaluating 14-Day Ahead Weather Predictions in the City of Manila: A Comparative Multivariate Study Using ARIMAX and Lagged Multiple Linear Regression

---

## Research Overview
This research compares a recursive stochastic approach (ARIMAX) against a direct deterministic approach (Lagged Multiple Linear Regression) to determine which better maintains predictive stability over a 14-day horizon. The models are evaluated using statistical tools such as Hotellings $T^2$ Test and Diebold-Mariano Test and standard metrics such as MAE and RMSE.

---

## Methodology and Framework
1. **Preprocessing and Dimensionality Reduction:**
* **Data Source:** 15 meteorological parameters sourced from the Open-Meteo API.
* **Stationarity:** All features subjected to Augmented Dickey-Fuller Testing and non-staionary variables (Dew Point) were first-order differenced.
* **PCA:** The 12 predictors were reduced to 7 Principal Components, retaining 93% of the explained variance.

2. **Forecasting Models:**
* **ARIMAX:** Utilizes auto_arima for optimal (p,d,q) selection.
* **Direct Multi-Step LMLR:** A high-dimensional framework using 168 independent linear regressions. Each model is trained to map a 65-predictor feature (7 PC lags + 3 label lags) directly to a specific lead time (h=1,2,3,...,14), to avoid recursive error propagation.

3. **Seasonal Partitioning:**
To account for the distinct weather patterns in the Philippines, the data is partitioned into four folds:
* **Habagat**
* **Transition**
* **Amihan**
* **Dry Season**

4. **Evaluation and Validation:**
* **Multivariate Validation:** Hotelling's $T^2$ test to detect mean vector drift in 14-day forecasts.
* **Statistical Superiority:** Diebold-Mariano Test to identify if the ARIMAX's stochastic advantage is statistically significant over LMLR.
* **Accuracy Metrics:** RMSE and MAE across all 14-day predictions.

---

## 📊 Summary of Results

The study evaluated the 14-day predictive accuracy across four distinct seasonal folds. The **ARIMAX-PCA** (Stochastic) model was compared against the **Direct Multi-Step LMLR** (Deterministic Baseline).

| Season | Best Performing Model | RMSE (Avg) | Statistical Significance (DM Test) |
| :--- | :--- | :--- | :--- |
| **Habagat** | **ARIMAX-PCA** | 0.82°C | Significant ($p < 0.05$) |
| **Transition** | **ARIMAX-PCA** | 0.74°C | Significant ($p < 0.05$) |
| **Amihan** | **Tie** | 0.68°C | Not Significant ($p > 0.05$) |
| **Dry Season** | **LMLR** | 0.62°C | Not Significant ($p > 0.05$) |

---

## Academic Context
**Institution:** Southern Luzon State University <br>
**College:** College of Arts and Sciences <br>
**Degree:** Bachelor of Science in Mathematics <br>
**Date:** April 2026 <br>

### **Course Compliance**
This research serves as a partial requirement for the following courses:
* **MAT25 (Statistical Modelling):** ARIMAX Modelling, Multiple Linear Regression, Partial Autocorrelation Function
* **MAT26 (Applied Multivariate Analysis):** Principal Component Analysis, Hotellings $T^2$ Test

---

## Research Team
This study is a collaborative effort by a six-member research group.

* **[Sieg Gabriel Sola](https://www.linkedin.com/in/sieg-gabriel-sola) (Technical Lead):** Responsible for the mathematical framework, Python implementation, ARIMAX architecture, and statistical diagnostics (PCA, PACF, Hotelling’s $T^2$).
* **Co-Authors:** Christian Mark Regencia, Dan Lloyd Otico, Jerica Sabido, Jorgia Sabido, Keziah Nicole Lingahan (Literature Review, Theoretical Framework, and Documentation).

---
