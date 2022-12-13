# Logistic Regression

Logistic regression is a type of supervised learning algorithm used for classification. It is a linear model that is used to predict the probability of a binary outcome based on the value of one or more predictor variables.

In logistic regression, the dependent variable is binary, meaning it can take on only two values, such as "Yes" or "No". The goal is to use one or more independent variables (also known as predictor variables) to predict the probability that the dependent variable will take on one of the two values.

Logistic regression is a powerful tool for classification and prediction, and it is widely used in many different fields, including finance, marketing, and medicine. It is particularly useful when the dependent variable is binary, as it allows us to estimate the probability of a particular outcome.

### How does it work?

Logistic regression is a linear model, which means it is based on a linear combination of the predictor variables. In other words, the predicted probability is calculated by taking a weighted sum of the predictor variables, where the weights are learned from the data.

The predicted probability is then transformed into a binary outcome using the logistic function. The logistic function has a "S" shape, and it maps any real-valued number to a value between 0 and 1. This means that the predicted probability, which can be any value between 0 and 1, is transformed into a binary outcome of 0 or 1.

To train the logistic regression model, we need a training dataset that includes the predictor variables and the binary outcome. The model is trained by adjusting the weights of the predictor variables so that the predicted probabilities are as close as possible to the actual values of the binary outcome. This is typically done using an optimization algorithm, such as gradient descent, which is used to minimize the error between the predicted probabilities and the actual values.

Once the model is trained, it can be used to predict the probability of the binary outcome for new data points. The predicted probability can then be transformed into a binary outcome using the logistic function, allowing us to make predictions about the outcome.

### Example

Here is a simple example of how logistic regression can be used for classification in Python using the scikit-learn library:

```python
# Import necessary libraries
from sklearn.linear_model import LogisticRegression

# Define the training set
X = [[30, 40], [20, 30], [40, 50], [35, 45], [25, 35]]
y = [0, 0, 1, 1, 0]

# Define the classifier
clf = LogisticRegression()

# Train the classifier using the training set
clf.fit(X, y)

# Predict the class of a new data point
new_data_point = [30, 40]
prediction = clf.predict([new_data_point])
print(prediction) # Output: [0]
```

This code will train a logistic regression classifier using the training set defined in `X` and `y`, and then use the trained classifier to predict the class of the new data point `[30, 40]`. The output of the code should be `[0]`, indicating that the new data point is predicted to be in class 0.

Note that this is a very simple example to illustrate how logistic regression works, and in practice the algorithm can be used with more complex data sets and a larger number of classes.
