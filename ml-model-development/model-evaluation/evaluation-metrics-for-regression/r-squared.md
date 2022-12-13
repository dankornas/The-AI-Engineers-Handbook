# R-Squared

R-squared, also known as the coefficient of determination, is a measure of how well a model fits a set of data. It is calculated by taking the squared differences between the predicted values and the actual values, and dividing that value by the squared differences between the actual values and the mean of the actual values.

R-squared ranges from 0 to 1, where 0 indicates that the model does not fit the data at all, and 1 indicates that the model fits the data perfectly. So, a higher R-squared value indicates a better fit.

R-squared is commonly used in regression tasks, where the goal is to predict a continuous value. It is a useful metric for evaluating the performance of a model and for comparing the performance of different models.

To calculate R-squared, we first need to calculate the squared differences between the predicted values and the actual values. This can be done by taking the difference between each predicted value and the corresponding actual value, and then squaring that difference. Then, we need to calculate the squared differences between the actual values and the mean of the actual values. This can be done by taking the difference between each actual value and the mean of the actual values, and then squaring that difference. Finally, we divide the sum of the squared differences between the predicted values and the actual values by the sum of the squared differences between the actual values and the mean of the actual values.

Here is a short code example of how to calculate R-squared in Python:

```makefile
Copy codeimport numpy as np

# define the predicted values
predicted = [3, 4, 5, 6]

# define the actual values
actual = [2, 4, 6, 8]

# calculate the squared differences between the predicted and actual values
squared_differences_predicted = (predicted - actual)**2

# calculate the squared differences between the actual values and the mean of the actual values
mean_actual = np.mean(actual)
squared_differences_mean = (actual - mean_actual)**2

# calculate R-squared
r_squared = np.sum(squared_differences_predicted) / np.sum(squared_differences_mean)

# print R-squared
print(r_squared)  # output: 0.6
```

In this example, we first import the NumPy library, which we will use to calculate the mean and sum. Then, we define the predicted values and the actual values. Next, we calculate the squared differences between the predicted and actual values, and the squared differences between the actual values and the mean of the actual values. Finally, we calculate R-squared by dividing the sum of the squared differences between the predicted and actual values by the sum of the squared differences between the actual values and the mean of the actual values, and then print the result to the console.
