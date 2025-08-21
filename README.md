## About the Project

This project primarily focuses on applying an LSTM model to weather data using Python.

### About the dataset
 The objective is to forecast the mean daily temperature (meantemp) for a fourteen-day horizon using input features 'humidity', 'meantemp', 'wind_speed', and 'meanpressure'.

<img width="527" height="263" alt="image" src="https://github.com/user-attachments/assets/8e8c74a0-0d5b-40e9-a370-44a683d279d7" />

### Descriptive Statistics

* humidity: The average humidity is approximately 60.42, with a standard deviation of around 16.96. Humidity ranges from a minimum of 13.43 to a maximum of 98.

* meantemp: The average mean temperature is about 25.23, with a standard deviation of approximately 7.34. The temperature varies between a minimum of 6 and a maximum of 38.71.

* wind_speed: The average wind speed is roughly 6.90, with a standard deviation of about 4.51. Wind speed values range from a minimum of 0 to a maximum of 42.22.

* meanpressure: The average mean atmospheric pressure is approximately 10.11, with a standard deviation of around 1.75. Mean pressure varies from a minimum of -0.03 to a maximum of 76.79.

<img width="580" height="652" alt="image" src="https://github.com/user-attachments/assets/ab0db571-531f-457a-a2cd-846e3b0fda77" />

### Model Architecture

* The model creation follows a sequential approach facilitated by the Keras library.
* It begins with the instantiation of a Sequential model, serving as a linear stack for subsequent layers.
* An LSTM layer is added, with the following characteristics:
      * It consists of a user-defined number of units, which act as specialized memory cells.
      * The hyperbolic tangent activation function is applied to these memory cells, enabling the detection of sequential patterns.
      * The input shape parameter accounts for the temporal dimension of the data and the attributes associated with each time step.
* A densely connected layer is subsequently included:
      * The provided units parameter determines the number of neurons in this layer.
      * This layer contributes to the further refinement of processed information.
* During compilation, the model is configured with:
      * The "RMSprop" optimization algorithm to facilitate efficient training.
      * The mean squared error (MSE) loss function, suitable for regression tasks, to quantify the disparity between predicted and actual values.

### Model Performance

<img width="757" height="562" alt="image" src="https://github.com/user-attachments/assets/d22a01c1-dc72-451f-a085-c3064fc8416a" />

Please refer to the notbook for more informtaion.




