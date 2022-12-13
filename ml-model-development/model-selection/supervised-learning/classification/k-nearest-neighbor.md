# K-Nearest Neighbor

### What is it?

K-nearest neighbor (KNN) is a simple and effective method for classification and regression. In the case of classification, the algorithm will find the K data points in the training set that are closest to the new data point, and it will assign the new data point to the class to which the majority of these K data points belong. In the case of regression, the algorithm will simply take the average of the K nearest data points to make its prediction.

### How does it work?

The KNN algorithm works by calculating the distance between the new data point and all the points in the training set. The distance is typically measured using the Euclidean distance, which is the straight-line distance between two points. The algorithm then sorts all the points in the training set by their distance from the new data point, and it chooses the K points that are closest to it.

Once the K nearest points have been identified, the KNN algorithm can make its prediction. In the case of classification, the algorithm will assign the new data point to the class to which the majority of the K nearest points belong. For example, if K=3 and the three nearest points are all in the class "dog," the algorithm will predict that the new data point is also in the class "dog." In the case of regression, the algorithm will take the average of the K nearest points to make its prediction.

### Example

Let's say we have a training set with three data points, and we want to use KNN to classify a new data point.

Training set:

(1,1) -> class A

(2,2) -> class B

(3,3) -> class B

New data point:

(2,1)

To classify the new data point using KNN, we would first calculate the distance between the new data point and each of the points in the training set. Using the Euclidean distance, we get the following distances:

(1,1) -> 1.4142135623730951

(2,2) -> 1.4142135623730951

(3,3) -> 2.23606797749979

Next, we would sort the points in the training set by their distance from the new data point, and we would choose the K=3 points that are closest to it. In this case, the three closest points are all in class B, so the KNN algorithm would predict that the new data point is also in class B.

This is a very simple example to illustrate how KNN works, but in practice the algorithm can be used with more complex data sets and a larger number of classes.



Here is an example of how KNN can be implemented using scikit-learn in Python:

```python
# Import necessary libraries
from sklearn.neighbors import KNeighborsClassifier

# Define the training set
X = [[1,1], [2,2], [3,3]]
y = ['A', 'B', 'B']

# Define the classifier
clf = KNeighborsClassifier(n_neighbors=3)

# Train the classifier using the training set
clf.fit(X, y)

# Predict the class of the new data point
new_data_point = [2, 1]
prediction = clf.predict([new_data_point])
print(prediction) # Output: ['B']
```

This code will train a KNN classifier using the training set defined in `X` and `y`, and then use the trained classifier to predict the class of the new data point `[2, 1]`. The output of the code should be `['B']`, indicating that the new data point is predicted to be in class B.
