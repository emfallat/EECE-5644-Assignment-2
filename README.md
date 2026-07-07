# EECE 5644 Assignment 2

## What this project does
This repository takes the Telco Customer dataset (7,043 customers) and:
1. Profiles the raw data to confirm the target variable (`MonthlyCharges`) is continuous
   and to verify that the service columns are clean 0/1 indicators with no missing values.
2. Defines a target (`MonthlyCharges`) and ten service-related predictors (phone, internet, and other add-on indicators).
3. Splits the data into an 80/20 train/test set with a fixed random seed for reproducibility.
4. Fits a multivariable linear regression, ŷ = w₀ + Σᵢ wᵢxᵢ, on the training set and reports the intercept and all ten coefficients.
5. Evaluates the model on the test set using R², MAE, and RMSE.
6. Builds a simple baseline model from a single "count of add-ons" feature built from the same ten columns, and then compares it against the multivariable model on the identical train/test split.
7. Interprets the fitted coefficients in plain business terms (each weight ~= monthly price of that service) and uses the trained model to predict the expected monthly bill for a new, hypothetical customer bundle.

## Repository contents
| File | Description |
|---|---|
| `telco.ipynb` | Analysis notebook, organized by step number |
| `telco.csv` | Raw Telco Customer dataset |
| `data_dictionary.md` | Column-by-column description of the dataset and encoded features |
| `findings_summary.md` | Coefficient interpretation, baseline comparison, and sample prediction |
| `requirements.txt` | Python library versions needed to reproduce this work |

## Dataset
**Telco Customer**: a dataset of customer account, service-subscription, and billing information from a telecom provider. Each add-on nudges the monthly bill upward, but not by the same amount. The goal is to determine, given which add-on services a customer subscribes to, what monthly charge should we expect them to
pay?


## How to run
1. Clone this repository (has `telco.csv` in it).
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate    # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Open `telco.ipynb` in Jupyter or VS Code.
4. Run all cells from top to bottom (**Restart Kernel + Run All**)
6. The notebook will print the fitted intercept and coefficients, the test-set evaluation metrics, the baseline comparison, and a sample prediction for a hypothetical customer.

## Summary of findings
*(See `findings_summary.md` for the full write-up with coefficient interpretation and
supporting numbers.)*