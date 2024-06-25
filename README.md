# Multioutput Regression using Linear Regression

## Overview
This project implements multioutput regression using linear regression techniques, allowing prediction of multiple continuous target variables simultaneously.

## Features
- Utilizes `MultiOutputRegressor` with linear regression as the base estimator.
- Evaluates using Mean Squared Error (MSE) and R-squared metrics.
- Includes an example demonstrating usage with sample data.

## Requirements
- Python 3.x
- Required libraries: scikit-learn, numpy, pandas

## Installation
Clone the repository and install dependencies:
```bash
git clone <repository-url>
cd project-directory
pip install -r requirements.txt
```

## Data Format
### Input Features
Input features should be structured as a 2D array (matrix) where each row represents a sample and each column represents a feature.

### Output/Target Variables
Target variables for multioutput regression should be structured as a 2D array where each row corresponds to the same sample as the input features, and each column represents a different target variable to predict.

## Training
To train the multioutput regression model:
```python
from sklearn.multioutput import MultiOutputRegressor
from sklearn.linear_model import LinearRegression

# Assuming X_train and y_train are your input and target variables
model = MultiOutputRegressor(LinearRegression())
model.fit(X_train, y_train)
```

## Evaluation
To evaluate the model, calculate Mean Squared Error (MSE) and R-squared:
```python
from sklearn.metrics import mean_squared_error, r2_score

# Assuming X_test and y_test are your test data
y_pred = model.predict(X_test)

mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print(f"Mean Squared Error: {mse}")
print(f"R-squared: {r2}")
```
### Interpreting the Results
Interpret the MSE and R-squared values to gauge model performance. 
MSE should be minimized, while R-squared should be close to 1 for good fit.


## License
Specify the license under which your project is distributed.
