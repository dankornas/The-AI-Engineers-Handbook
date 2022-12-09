# Naive Bayes

The Naive Bayes model is a simple probabilistic model that makes predictions based on the application of Bayes' theorem with strong (naive) independence assumptions between the features. In other words, the Naive Bayes model assumes that the presence (or absence) of a particular feature of a class is unrelated to the presence (or absence) of any other feature.

For example, if we are trying to predict whether a person is male or female based on their height, weight, and hair length, the Naive Bayes model would assume that the height, weight, and hair length of the person are independent of one another. This allows for a very simple and efficient prediction method, as we can just calculate the probabilities of each class (male or female) based on the individual feature probabilities and apply Bayes' theorem to compute the final probabilities.

The predicted class is then the one with the highest probability, according to the model. It's called "naive" because the model makes a strong assumption that is rarely true in real-world data, but despite this, the model often performs well in practice.

### Example

To use the Naive Bayes model in Python, we can use the `sklearn` library. Here is an example of how we might predict the gender of a person based on their height, weight, and hair length using the Naive Bayes model in Python:

```python
# Import the necessary modules
from sklearn.naive_bayes import GaussianNB

# Create the model
model = GaussianNB()

# Train the model with the training data
# The training data is a matrix with three columns (height, weight, hair length)
# and a label column (gender)
model.fit(training_data, training_labels)

# Use the trained model to make predictions on new data
# The new data is a matrix with the same three columns (height, weight, hair length)
predictions = model.predict(new_data)

# The predictions will be a vector of labels (either "male" or "female")
# corresponding to each row of the new data
```

In this example, the model first trains on the given training data by calculating the probabilities of each feature (height, weight, hair length) for each class (male or female). Then, when making predictions on new data, the model applies Bayes' theorem using the calculated probabilities to predict the class with the highest probability for each row of data.

### Naive Bayes Model from scratch

```python
# Import necessary modules
import numpy as np

# Define the Naive Bayes class
class NaiveBayes:
    # Initialize the model
    def __init__(self):
        self.mean = None
        self.var = None
        self.prior = None
    
    # Fit the model to the training data
    def fit(self, X, y):
        # Get the number of classes and the number of features
        n_classes = np.unique(y).size
        n_features = X.shape[1]
        
        # Calculate the mean and variance of each feature for each class
        self.mean = np.zeros((n_classes, n_features))
        self.var = np.zeros((n_classes, n_features))
        for c in range(n_classes):
            X_c = X[y == c]
            self.mean[c, :] = np.mean(X_c, axis=0)
            self.var[c, :] = np.var(X_c, axis=0)
        
        # Calculate the prior probabilities of each class
        self.prior = np.zeros(n_classes)
        for c in range(n_classes):
            self.prior[c] = np.mean(y == c)
    
    # Make predictions on new data
    def predict(self, X):
        # Get the number of classes and the number of features
        n_classes = self.prior.size
        n_features = X.shape[1]
        
        # Calculate the likelihood of each feature for each class
        likelihood = np.zeros((n_classes, n_features))
        for c in range(n_classes):
            for f in range(n_features):
                likelihood[c, f] = (1 / np.sqrt(2 * np.pi * self.var[c, f])) * np.exp(-0.5 * (X[:, f] - self.mean[c, f]) ** 2 / self.var[c, f])
        
        # Calculate the posterior probabilities of each class for each sample
        posterior = np.zeros((X.shape[0], n_classes))
        for c in range(n_classes):
            posterior[:, c] = np.prod(likelihood[c, :], axis=1) * self.prior[c]
        
        # Return the predicted class for each sample
        return np.argmax(posterior, axis=1)

# Create the model
model = NaiveBayes()

# Train the model with the training data
# The training data is a matrix with three columns (height, weight, hair length)
# and a label column (gender)
model.fit(training_data, training_labels)

# Use the trained model to make predictions on new data
# The new data is a matrix with the same three columns (height, weight, hair length)
predictions = model.predict(new_data)

# The predictions will be a vector of labels (either "male" or "female")
# corresponding to each row of the new data
```

In this example, the Naive Bayes class implements the model from scratch, using the mean and variance of each feature for each class to calculate the likelihood of each feature, and then applying Bayes' theorem to calculate the posterior probabilities of each class for each sample. The predicted class is then the one with the highest posterior probability for each sample.

This implementation is slightly more general than the `sklearn` implementation, as it allows for multi-class classification, whereas the `sklearn` implementation only allows for binary classification. However, the `sklearn` implementation is more efficient and optimized for real-world use.

#### Fit

In the `fit` method of the Naive Bayes class, the model is trained on the given training data. This method performs the following steps:

1. It calculates the number of classes and the number of features in the training data.
2. It calculates the mean and variance of each feature for each class. This is done by splitting the training data into subsets for each class and then calculating the mean and variance of each feature in each subset.
3. It calculates the prior probabilities of each class. This is done by counting the number of samples in each class and dividing by the total number of samples to compute the relative frequency of each class.

After these steps are completed, the `fit` method stores the calculated values (mean, variance, and prior probabilities) in the model, which will be used later to make predictions. This training phase is an important step for the Naive Bayes model, as it allows the model to learn the statistical properties of the training data and make informed predictions on new data.

#### Predict

In the `predict` method of the Naive Bayes class, the trained model is used to make predictions on new data. This method performs the following steps:

1. It calculates the number of classes and the number of features in the new data.
2. It calculates the likelihood of each feature for each class. This is done by using the mean and variance values that were calculated during the training phase, and applying the normal distribution formula to compute the likelihood of each feature for each class.
3. It applies Bayes' theorem to calculate the posterior probabilities of each class for each sample in the new data. This is done by multiplying the likelihood of each feature for each class with the prior probabilities of each class, and then normalizing the resulting probabilities to sum to 1.
4. It returns the predicted class for each sample, which is the class with the highest posterior probability.

After these steps are completed, the `predict` method returns a vector of predicted classes, one for each sample in the new data. This allows us to evaluate the performance of the model and use it to make predictions on unseen data.
