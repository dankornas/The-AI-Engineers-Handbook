# Bias & Variance

Bias and variance are two important concepts in machine learning that describe the error in a model's predictions.

## Bias

Bias is the difference between a model's expected predictions and the true values in the data. A high bias means that the model's predictions are consistently far from the true values, which indicates that the model is oversimplified and is unable to capture the underlying pattern in the data.

### Example

Imagine you are training a machine learning model to predict the price of a house based on its size, location, and other features. You have a dataset of 1000 houses, with their size, location, and other features, as well as their prices. You train a linear regression model on this dataset, and evaluate its performance on the training data. The model performs well on the training data, with a low mean squared error (MSE) and high R-squared value.

However, when you evaluate the model on unseen data (e.g. a test set or new data), you find that it performs poorly. The MSE is high and the R-squared value is low, indicating that the model is not accurately predicting the prices of the unseen houses.

When you analyze the model's predictions, you find that they are consistently lower than the true values. For example, if the true price of a house is $500,000, the model's prediction may be $450,000. This indicates that the model has a high bias, because it consistently underestimates the true prices of the houses.

This is an example of bias, because the model is oversimplified and is unable to capture the underlying pattern in the data. In this case, the model may have ignored important features that are relevant for predicting house prices, and therefore is unable to accurately predict the prices of unseen houses.

## Variance

Variance is the amount of variability in a model's predictions. A high variance means that the model's predictions are very sensitive to small changes in the training data, which indicates that the model is overcomplicated and is fitting to the noise in the data rather than the underlying pattern.

### Example

Imagine you are training a machine learning model to predict the price of a house based on its size, location, and other features. You have a dataset of 1000 houses, with their size, location, and other features, as well as their prices. You train a decision tree model on this dataset, and evaluate its performance on the training data. The model performs well on the training data, with a low mean squared error (MSE) and high R-squared value.

However, when you evaluate the model on unseen data (e.g. a test set or new data), you find that it performs poorly. The MSE is high and the R-squared value is low, indicating that the model is not accurately predicting the prices of the unseen houses.

When you analyze the model's predictions, you find that they vary greatly depending on the specific training data used to train the model. For example, if you train the model on a different subset of the training data, the predictions may be significantly different from the previous ones. This indicates that the model has a high variance, because it is very sensitive to the specific training data used.

This is an example of variance, because the model is overcomplicated and is fitting to the noise in the data rather than the underlying pattern. In this case, the model may have learned to fit some outliers in the training data, or may have picked up on some random correlations that do not hold for the unseen data.

## Bias - Variance Trade Off

Together, bias and variance form the bias-variance tradeoff, which states that a model with low bias and high variance will overfit to the training data, while a model with high bias and low variance will underfit to the training data. To achieve a good balance between bias and variance, and therefore good performance on unseen data, it is important to find the right model complexity for the specific dataset and task.
