# Self-Driving-Car
This project demonstrates the implementation of a self-driving car using deep learning techniques for predicting actions in the Udacity car simulator. By training a convolutional neural network (CNN) model, the car learns to navigate through the scenarios in the simulator.


## Introduction

Self-driving cars represent a significant advancement in autonomous vehicle technology. This project focuses on utilizing deep learning algorithms to predict appropriate actions for steering the car within the simulated environment provided by Udacity.

## Features
- Data Preprocessing:
Loaded driving log data from a CSV file generated by the Udacity car simulator.
Extracted file names for center, left, and right camera images.
Applied preprocessing steps including cropping, resizing, and normalization to prepare input images.

- Data Augmentation:
Implemented random augmentation techniques such as panning, zooming, brightness adjustment, and flipping to increase dataset variability.
Balanced the dataset by removing excess samples from bins of steering angles.

- Model Training:
Split the dataset into training and validation sets using sklearn's train_test_split function.
Developed a convolutional neural network (CNN) model using TensorFlow and Keras.
The model architecture consists of convolutional layers followed by fully connected layers.
Compiled the model using the Adam optimizer and mean squared error (MSE) loss function.

- Socket.IO Server Integration:
Established a bidirectional communication link between the self-driving car controller and the Udacity car simulator using Socket.IO.
Created a Flask application to host the Socket.IO server.
Implemented functions to preprocess images received from the simulator and predict steering angles using the trained model.

- Real-time Control:
Received telemetry data including speed and camera images from the simulator via Socket.IO.
Preprocessed the received images and fed them into the trained model to predict steering angles.
Adjusted throttle based on the car's speed relative to a predefined speed limit.
Sent steering angle and throttle commands back to the simulator to control the car in real-time.

## Steps to Reproduce

1. Clone the repository to your local machine.
2. Download the Udacity car simulator from [here](https://github.com/udacity/self-driving-car-sim).
3. Install the required dependencies.
4. Run the Python script `main.ipynb` to train the deep learning model.
5. Launch the Udacity car simulator and select the autonomous mode.
6. Once trained, run the command in cmd `python drive.py`

https://github.com/wannasleepforlong/Self-Driving-Car/assets/109717763/bfc4a06c-d17a-428d-a9f4-f756ef81850a

