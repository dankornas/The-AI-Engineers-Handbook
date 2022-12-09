# Linear Regression

Linear regression is a common method in machine learning that is used to model the relationship between a dependent variable, which is the variable that we are trying to predict, and one or more independent variables, which are the factors that are used to predict the value of the dependent variable. In a linear regression model, the relationship between the dependent and independent variables is represented by a straight line, which is called the regression line. This line is calculated by finding the values of the slope and intercept that minimize the sum of the squares of the differences between the observed values of the dependent variable and the values predicted by the model. Once these values have been determined, the regression line can be used to make predictions about the value of the dependent variable for any given value of the independent variable.

### Example

Let's say we're trying to predict the price of a house based on its size. In this case, the dependent variable would be the price of the house, and the independent variable would be the size of the house. To create our linear regression model, we would first collect data on the prices and sizes of a number of houses. Then, we would plot these data points on a scatter plot, with the size of the house on the x-axis and the price on the y-axis. This scatter plot would likely show a roughly linear relationship between the size of the house and its price, with larger houses tending to have higher prices.

Next, we would calculate the regression line that best fits the data. This line would be determined by finding the values of the slope and intercept that minimize the sum of the squares of the differences between the observed prices of the houses and the prices predicted by the model. Once we have this line, we can use it to make predictions about the price of a house based on its size. For example, if the regression line has a slope of $100,000 and an intercept of $200,000, we could predict that a house with a size of 1,500 square feet would have a price of $300,000 (1,500 x $100,000 + $200,000), and a house with a size of 2,000 square feet would have a price of $400,000 (2,000 x $100,000 + $200,000), and so on.



```python
# First, we import the necessary libraries
from sklearn.linear_model import LinearRegression
import numpy as np

# Next, we define the data for the model
# In this case, we have two independent variables (size and number of bedrooms)
# and one dependent variable (price)
size = [1, 2, 3, 4, 5]
bedrooms = [1, 1, 2, 2, 3]
price = [100, 150, 200, 250, 300]

# Then, we convert the data to numpy arrays
X = np.array([size, bedrooms]).T
y = np.array(price)

# Next, we create the linear regression model and fit it to the data
model = LinearRegression()
model.fit(X, y)

# Now, we can use the model to make predictions
# For example, let's predict the price of a house with a size of 3 and 1 bedroom
size = 3
bedrooms = 1
X_new = np.array([[size, bedrooms]])
prediction = model.predict(X_new)
print(prediction)  # This should output approximately [200]
```

In this example, we first import the necessary libraries, then define the data for the model. We then convert the data to numpy arrays, create a `LinearRegression` object and fit it to the data using the `fit` method. Finally, we use the `predict` method of the model to make a prediction for a new data point.
