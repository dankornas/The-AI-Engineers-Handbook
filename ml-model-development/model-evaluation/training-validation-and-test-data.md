# Training, validation, and test data

### Splitting the data

When training a machine learning model, it is common to split the data into three sets: training, validation, and testing. The training set is used to train the model, the validation set is used to evaluate the performance of the model on unseen data and adjust its hyperparameters, and the testing set is used to evaluate the final performance of the model.

The process of splitting the data into these sets typically involves randomly selecting a portion of the data to be used for each set. For example, the data might be split into 70% training data, 20% validation data, and 10% testing data. The exact proportions will depend on the size and nature of the data, as well as the specific requirements of the machine learning task.

Once the data has been split into the appropriate sets, the model can be trained on the training set. During training, the model's performance on the validation set is monitored, and the hyperparameters of the model are adjusted to improve its performance on the validation set. Once the model is trained and its hyperparameters are set, it can be evaluated on the testing set to assess its performance on unseen data.

### The purpose of splitting

When training a machine learning model, it is important to evaluate the model's performance on unseen data to ensure that it is not overfitting to the training data. Overfitting occurs when a model performs well on the training data but poorly on new, unseen data. One way to avoid overfitting is to split the data into training, validation, and testing sets, and use the validation set to tune the model's hyperparameters.

The training set is used to train the model, which involves adjusting the model's parameters to minimize the error on the training data. The validation set is used to evaluate the model's performance on unseen data, and the hyperparameters of the model are adjusted to improve its performance on the validation set. The testing set is used to evaluate the final performance of the model, and is only used once the model's hyperparameters have been set.

The process of splitting the data into training, validation, and testing sets helps to ensure that the model is not overfitting to the training data, and that its performance on unseen data is as good as possible. This is important because a model that overfits to the training data will not generalize well to new, unseen data, and will therefore be less useful in real-world applications.
