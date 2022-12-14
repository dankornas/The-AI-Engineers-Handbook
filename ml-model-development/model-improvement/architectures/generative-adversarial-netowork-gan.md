# Generative Adversarial Netowork (GAN)

### What is it?

Generative adversarial networks (GANs) are a type of neural network architecture that is used for unsupervised learning. GANs consist of two networks: a generative network and a discriminative network. The generative network learns to generate new data samples that are similar to a training dataset, while the discriminative network learns to classify whether a sample is real (from the training dataset) or fake (generated by the generative network).

The two networks are trained together in a competition, where the goal of the generative network is to generate samples that are indistinguishable from real samples, and the goal of the discriminative network is to correctly identify real and fake samples. This competition forces the generative network to improve its ability to generate realistic samples, while also improving the discriminative network's ability to distinguish real from fake samples.

### How does it work?

The generative network takes as input a random noise vector and generates a synthetic data sample.

The discriminative network takes as input a data sample (real or fake) and produces a classification (real or fake).

The two networks are trained together by alternating between the following steps:

* The generative network generates a synthetic sample and the discriminative network classifies it as real or fake.
* The discriminative network receives a real sample from the training dataset and a fake sample from the generative network, and tries to classify them correctly.
* The weights of both networks are updated based on their performance on the classification task.

This process is repeated for multiple training iterations, and the generative network gradually improves its ability to generate realistic samples.

### Example

```python
# Import necessary modules
from keras.models import Model
from keras.layers import Input, Dense, LeakyReLU, BatchNormalization, Reshape
from keras.optimizers import Adam

### Creating the generator ###
# Define the input layer
input_noise = Input(shape=(noise_dim,))

# Define the generator network
x = Dense(units=256)(input_noise)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
x = Dense(units=512)(x)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
x = Dense(units=1024)(x)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
x = Dense(units=2048)(x)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
output_data = Dense(units=data_dim, activation='tanh')(x)

# Define the model
generator = Model(inputs=input_noise, outputs=output_data)

### Creating the discriminator ###
# Define the input layer
input_data = Input(shape=(data_dim,))

# Define the discriminator network
x = Dense(units=1024)(input_data)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
x = Dense(units=512)(x)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
x = Dense(units=256)(x)
x = LeakyReLU(alpha=0.2)(x)
x = BatchNormalization()(x)
output_classification = Dense(units=1, activation='sigmoid')(x)

# Define the model
discriminator = Model(inputs=input_data, outputs=output_classification)

### Creating the GAN Model ###
# Define the GAN model
gan_input = Input(shape=(noise_dim,))
generated_data = generator(gan_input)
gan_output = discriminator(generated_data)
gan = Model(inputs=gan_input, outputs=gan_output)

# Compile the GAN model
optimizer = Adam(lr=0.0002, beta_1=0.5)
gan.compile(loss='binary_crossentropy', optimizer=optimizer)
```
