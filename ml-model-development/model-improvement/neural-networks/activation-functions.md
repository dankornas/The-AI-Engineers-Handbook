# Activation Functions

An activation function is a function in a neural network that determines the output of a neuron given its input. The activation function is typically a non-linear function that takes the weighted sum of the inputs as input and produces a binary output (0 or 1) or a continuous output in a range from 0 to 1 or from -1 to 1.

Activation functions are important in neural networks because they introduce non-linearity, which allows the network to learn more complex relationships between the inputs and the outputs. Some common activation functions include the sigmoid function, the hyperbolic tangent function, and the rectified linear unit (ReLU) function.

In a neural network, the activation function is applied element-wise to the output of each neuron, and the resulting output is passed to the next layer of neurons in the network. The choice of activation function can have a significant impact on the performance of the neural network, so it is an important hyperparameter to tune.

### Example

Here is an example of using the rectified linear unit (ReLU) activation function in a neural network implemented in Python using the Keras library:

```python
import keras
from keras.models import Sequential
from keras.layers import Dense

# Define the model
model = Sequential()
model.add(Dense(units=64, activation='relu', input_dim=100))
model.add(Dense(units=10, activation='softmax'))

# Compile the model
model.compile(loss='categorical_crossentropy',
              optimizer='sgd',
              metrics=['accuracy'])

# Train the model
model.fit(x_train, y_train, epochs=5, batch_size=32)
```

In this example, we define a neural network with two dense layers. The first layer uses the ReLU activation function, which is defined as `activation='relu'` in the `Dense` layer. The second layer uses the softmax activation function, which is defined as `activation='softmax'` in the `Dense` layer. This allows the neural network to learn non-linear relationships between the input data and the outputs.
