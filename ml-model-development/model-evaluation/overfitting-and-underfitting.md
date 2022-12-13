# Overfitting & Underfitting

## Overfitting

Overfitting occurs when a model is too complex and captures too much of the random noise in the training data, instead of capturing the underlying pattern. This leads to poor performance on unseen data, because the model is not generalizable and does not accurately capture the underlying pattern.

### Example

Imagine you are training a machine learning model to predict the price of a house based on its size, location, and other features. You have a dataset of 1000 houses, with their size, location, and other features, as well as their prices. You train a linear regression model on this dataset, and evaluate its performance on the training data. The model performs well on the training data, with a low mean squared error (MSE) and high R-squared value.

However, when you evaluate the model on unseen data (e.g. a test set or new data), you find that it performs poorly. The MSE is high and the R-squared value is low, indicating that the model is not accurately predicting the prices of the unseen houses.

This is an example of overfitting, because the model has learned to fit the noise in the training data too closely, and is not generalizable to unseen data. In this case, the model may have learned to fit some outliers in the training data, or may have picked up on some random correlations that do not hold for the unseen data.

## Underfitting

Underfitting occurs when a model is too simple and does not capture the underlying pattern in the training data well enough. This also leads to poor performance on unseen data, because the model is not complex enough to accurately capture the pattern.

### Example

Using the same example as before, you are training a machine learning model to predict the price of a house based on its size, location, and other features. You have a dataset of 1000 houses, with their size, location, and other features, as well as their prices. You train a linear regression model on this dataset, but you only use the size and location features, and ignore other important features such as the number of bedrooms and bathrooms, the age of the house, etc.

When you evaluate the model on the training data, you find that it performs poorly, with a high MSE and low R-squared value. This indicates that the model is not accurately capturing the underlying pattern in the training data, and is unable to predict the prices of the houses accurately.

When you evaluate the model on unseen data (e.g. a test set or new data), you find that it performs even worse. The MSE is higher and the R-squared value is lower, indicating that the model is not generalizable and does not perform well on unseen data.

This is an example of underfitting, because the model is too simple and does not have enough features to accurately capture the underlying pattern in the data. In this case, the model may have ignored important features that are relevant for predicting house prices, and therefore is unable to accurately predict the prices of unseen houses.

