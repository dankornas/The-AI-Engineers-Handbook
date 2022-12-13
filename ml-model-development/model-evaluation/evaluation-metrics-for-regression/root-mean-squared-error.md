# Root Mean Squared Error

The root mean squared error (RMSE) is a measure of the difference between a model's predictions and the true values in the data. It is commonly used as a metric to evaluate the performance of a regression model, and is defined as the square root of the average of the squared differences between the predictions and the true values.

```python
import numpy as np

# Calculate the RMSE
y_true = [100, 50, 30, 20]
y_pred = [90, 50, 50, 30]
rmse = np.sqrt(np.mean((np.array(y_true) - np.array(y_pred))**2))

# Print the RMSE
print("RMSE:", rmse)
```

The RMSE is a measure of the average magnitude of the errors in a model's predictions, and is often used to compare the performance of different models. A lower RMSE indicates a better fit and more accurate predictions.
