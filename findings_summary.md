# Findings

## 1. Base plan cost (before add-ons)
$24.97

## 2. Individual add-on costs

| Service | Monthly Price ($) |
|---|---|
| InternetService_Fiber optic |     24.95 |
| PhoneService  |    20.04 |
| StreamingTV   |    9.98 |
| StreamingMovies   |    9.95 |
| OnlineSecurity  |     5.05 |
| TechSupport   |    5.03 |
| MultipleLines     |  5.01 |
| DeviceProtection   |    5.01 |
| OnlineBackup    |   4.98 |
| InternetService_No   |  -25.05 |

## 3. Add-ons
- InternetService_Fiber optic is the most expensive add-on at $24.95. 
- InternetService_No is the cheapest add-on (aka if you opt out of internet 
service, you save $25.05.)
- Besides opting out of internet service, the cheapest add-on would be OnlineBackup for $4.98

## 4. Customer Bill Cost
- InternetService_Fiber optic (24.95) + StreamingTV (9.98) + StreamingMovies (9.95) = $44.88
- Using Step 9 to make a prediction: 
    Expected monthly charge: $69.85
    Add-on cost: [44.87930567]
- Their bill will rise $44.88

## 5. Specific Bundle Monthly Charge
- Add-ons: PhoneService (20.04) + MultipleLines (5.01) + TechSupport (5.03) = 30.08
- Total bill/Monthly Charge:  $24.97 (base rate) + $30.08 = $55.05

## 6. Predicting Bill
Yes, knowing which services a customer has is meaningfully better than just knowing how many they have. In order to predict the bill more accurately, having the specific services can help us caluclate it better. This is because they're not all the same price, so the prediction of 2 additional services could be $44.99 (InternetService_Fiber optic + PhoneService) or $10.02 (MultipleLines + DeviceProtection) depending on which two, which is a very large difference. So knowing the specific services is meaningfully better for predicting the bill. 

## 7. Prediction Accuracy
Baseline (addon_count only):
  R²:   0.7009
  MAE:  $14.24
  RMSE: $16.46

Multivariable model:
  R²:   0.9988
  MAE:  $0.79
  RMSE: $1.05

-  R^2 = 0.9988 for multivariable shows that it is almost perfect 
- Dropping to MAE $0.79 and RMSE is $1.05 for multivariable shows that the model is predicitng monthly charges to within about a dollar on unseen customers, whihc is prettu good 
- R^2 this close to 1.0 shows that the MonthlyCharges is strongly correlated with these services 
- The predictions are very accurate on customers the model hasn't seen within less than a single dollar ($0.79) on average

## 8. Suprising Coefficients
- Nothing is suprising and they line up almost exactly with a sensible price list
- InternetService_No is negative but that makes sense as you would save money without that additional service 