# Data Dictionary — Telco Customer

(7,043 rows, 24 columns)

| Column | Type | Values | Description |
|---|---|---|---|
| `gender` | int64 (binary) | 0 / 1 | Customer's gender, encoded numerically. |
| `SeniorCitizen` | int64 (binary) | 0 / 1 | Whether the customer is a senior citizen. |
| `Partner` | int64 (binary) | 0 / 1 | Whether the customer has a partner. |
| `Dependents` | int64 (binary) | 0 / 1 | Whether the customer has dependents. |
| `tenure` | int64 (continuous) | 0–72 | Number of months the customer has been with the company. |
| `PhoneService` | int64 (binary) | 0 / 1 | Whether the customer subscribes to phone service. **Predictor.** |
| `MultipleLines` | int64 (binary) | 0 / 1 | Whether the customer has multiple phone lines. **Predictor.** |
| `OnlineSecurity` | int64 (binary) | 0 / 1 | Whether the customer subscribes to online security add-on. **Predictor.** |
| `OnlineBackup` | int64 (binary) | 0 / 1 | Whether the customer subscribes to online backup add-on. **Predictor.** |
| `DeviceProtection` | int64 (binary) | 0 / 1 | Whether the customer subscribes to device protection add-on. **Predictor.** |
| `TechSupport` | int64 (binary) | 0 / 1 | Whether the customer subscribes to tech support add-on. **Predictor.** |
| `StreamingTV` | int64 (binary) | 0 / 1 | Whether the customer subscribes to streaming TV add-on. **Predictor.** |
| `StreamingMovies` | int64 (binary) | 0 / 1 | Whether the customer subscribes to streaming movies add-on. **Predictor.** |
| `PaperlessBilling` | int64 (binary) | 0 / 1 | Whether the customer uses paperless billing. |
| `MonthlyCharges` | float64 (continuous) | e.g. 18.25–118.75 | **Target variable.** The customer's current monthly bill, in dollars. Originally loaded as `target` and renamed to `MonthlyCharges`. |
| `TotalCharges` | object → float64 | e.g. 29.85–8684.80 | Cumulative amount billed to the customer over their tenure. |
| `Churn` | int64 (binary) | 0 / 1 | Whether the customer has left the company. |
| `InternetService_Fiber optic` | int64 (binary) | 0 / 1 | Whether the customer has fiber optic internet. **Predictor.** |
| `InternetService_No` | int64 (binary) | 0 / 1 | Whether the customer has no internet service **Predictor.** |
| `Contract_One year` | int64 (binary) | 0 / 1 | Whether the customer is on a one-year contract |
| `Contract_Two year` | int64 (binary) | 0 / 1 | Whether the customer is on a two-year contract |
| `PaymentMethod_Credit card (automatic)` | int64 (binary) | 0 / 1 | Whether the customer pays by automatic credit card |
| `PaymentMethod_Electronic check` | int64 (binary) | 0 / 1 | Whether the customer pays by electronic check |
| `PaymentMethod_Mailed check` | int64 (binary) | 0 / 1 | Whether the customer pays by mailed check |

## Predictors used in the multivariable regression model (`X`)

```
PhoneService, MultipleLines, OnlineSecurity, OnlineBackup, DeviceProtection,
TechSupport, StreamingTV, StreamingMovies, InternetService_Fiber optic,
InternetService_No
```

## Target variable (`y`)

```
MonthlyCharges
```