# Neural Networks Predicting Weekly S&P 500 Index Prices Using Historical Observations

## Project Summary

This repository explores the use of neural networks to predict weekly S&P 500 index prices, leveraging historical financial time-series data. The project demonstrates data preprocessing, neural network construction, training, evaluation, and performance visualization using Python in a Jupyter Notebook.

## Features / Usage

- Data import and preprocessing for S&P 500 index historical prices
- Exploratory data analysis and visualization
- Construction and training of neural network models for price prediction
- Model evaluation and performance assessment (e.g., error metrics, charts)
- Easy-to-follow, modular Jupyter Notebook code and workflow

## How to Install / Run

1. **Clone the repository:**
    ```bash
    git clone https://github.com/StevenAmet/-Neural-Networks-Predicting-Weekly-S-P500-Index-Prices-using-Historical-Observations.git
    cd -Neural-Networks-Predicting-Weekly-S-P500-Index-Prices-using-Historical-Observations
    ```

2. **(Optional) Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    # On Windows:
    venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

3. **Install dependencies:**
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
    ```

4. **Run the notebook:**
    ```bash
    jupyter notebook
    ```
    Then open the notebook:
    ```
    Neural Networks Predicting Weekly S&P500 Index Prices using Historical Observations.ipynb
    ```

## Example Usage

```python
import pandas as pd
from tensorflow import keras
import matplotlib.pyplot as plt

# Load historical S&P 500 data
data = pd.read_csv("sp500-history.csv", parse_dates=['Date'])
# ... data processing ...

# Define a simple neural network
model = keras.Sequential([
    keras.layers.Dense(12, activation='relu', input_shape=(input_dim,)),
    keras.layers.Dense(1)
])

model.compile(optimizer='adam', loss='mean_squared_error')
model.fit(X_train, y_train, epochs=100, validation_split=0.2)

# Prediction and visualization
preds = model.predict(X_test)
plt.plot(y_test.values, label="Actual")
plt.plot(preds, label="Predicted")
plt.legend()
plt.show()
```

## Dependencies

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- tensorflow

**Install all at once:**
```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
```

## Author / License

**Author:** Steven Amet  


---

*This project demonstrates deep learning in financial time series with a focus on practical S&P 500 index prediction.*
