# City of Manila Seasonal Weather Forecasting
### Evaluating 14-Day Ahead Weather Predictions in the City of Manila: A Comparative Multivariate Study Using ARIMAX and Lagged Multiple Linear Regression

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

## Methodology
This project employs a **Two-Tier Architecture** to forecast 14 days of Manila’s weather:

1. **Dimensionality Reduction (PCA):** 12 meteorological variables were transformed into **7 Principal Components**, capturing >90% of atmospheric variance.
2. **Feature Engineering:** Optimal lag windows ($W$) were determined via **Partial Autocorrelation Function (PACF)** diagnostics for each seasonal fold.
3. **Forecasting Models:** * **ARIMAX:** A stochastic approach modeling.
    * **Lagged MLR:** A deterministic baseline using "Direct Training" to eliminate the error snowball effect.

---
