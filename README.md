# Handwritten character Recognition 
## Introduction
In this repository I used images of all alphabets and all digits. The images are used to train Convolutional Neural Network.
This model was used for prediction. The datset contains 36 classes: all digits and all lower case alphabets. The model gave
about 76%.

## Preprocessing Data
A filled form image was given with black boxes at top letf corner. Using the box has reference a mathematical formula for derived
to extract images. Thresholding and dilation were applied on these images to change the color with threshold and to maximize
the image for prediction using CNN.

## Network Graph
The CNN model

|       Layer        |         Description             |
|--------------------|-------------------------------- |
|Convolutional Layer |Filter Size:2*2 Filters:32       |
|Convolutional Layer |Filter Size:2*2 Filters:32       |
|Max Pooling Layer   |Pool Size:2*2                    |
|Convolutional Layer |Filter Size:2*2 Filters:32       |
|Convolutional Layer |Filter Size:2*2 Filter:32        |
|MaxPooling Layer    |Pool Size:2*2                    |
|Flatten             |Reshape 4D into 2D               |
|Dense               |Neural Network Layer, Neurons:128|
|Dropout             |Avoid overfitting, rate:0.2      |
|Dense               |Neural Network Layer, Neurons:36 |

## Training
1. Loss function: Cross Entropy
2. Optimizer: momemtum Gradient descent
3. used stochastic gradient descent

## Prediction
The model was saved. The saved model was used for prediction with the images obtained from during preprocessing.
