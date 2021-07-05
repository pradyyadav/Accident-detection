# Accident-detection using Autoencoders



[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

![GitHub contributors](https://img.shields.io/github/contributors/pradyyadav/Accident-detection)    ![GitHub last commit](https://img.shields.io/github/last-commit/pradyyadav/Accident-detection)

![ae](https://github.com/pradyyadav/Images/blob/main/autoencoder.png?raw=true)

##### A Spatio-temporal Autoencoder which consists of 3D Convolutional Layers and it detects accidents in real time videos.


##### Check this notebook out: ![accident_detection_using_autoencoder.ipynb](https://drive.google.com/file/d/1CX8vJMkC9b_tIw0EWR9WkuWkJlyojiUu/view?usp=sharing)


## Table of contents
- [Introduction](https://github.com/pradyyadav/Accident-detection#Introduction)
- [About](https://github.com/pradyyadav/Accident-detection#About)
- [Technologies](https://github.com/pradyyadav/Accident-detection#Technologies)
- [Setup](https://github.com/pradyyadav/Accident-detection#Setup)

## Introduction
A road traffic accident claims the lives of approximately 1.5 million people per year. Individuals, their families, and nations as a whole suffer significant economic damages as a result of road traffic accidents.     Most modern traffic monitoring systems rely on human observation and it's difficult to keep track of a large number of camera scenes at once and identify suspicious activities without missing something.

Our project focuses on incorporating a system which is able to detect an accident form video footage provided to it. Manually collecting datasets, training, validating, and checking the dataset for correct categorical results are all part of the implementation.

The model is designed to help out accident victims in need by timely detecting an accident.


##### Autoencoders

![auto](https://github.com/pradyyadav/Images/blob/main/ae.png?raw=true)

Autoencoders are an unsupervised learning technique in which neural networks areused to learn representations.  We will specifically design a neural network archi-tecture in which we will impose a bottleneck in the network, forcing a compressedknowledge representation of the original input.  This compression and subsequentreconstruction  would  be  extremely  difficult  if  the  input  features  were  completelyindependent of one another. However, if there is some structure in the data (for ex-ample, correlations between input features), this structure can be learned and thusleveraged when forcing the input through the network’s bottleneck.

A bottleneck limits the amount of information that can traverse the entire net-work, forcing the input data to be compressed in a learned manner.The ideal autoencoder model strikes a balance between the following factors:

1) Sensitive enough to the inputs to build an accurate reconstruction.
2) Insensitive to the inputs enough that the model does not simply memorise oroverfit the training data.


## About
First of all the data is collected from the largest video repository i.e. YouTube. The data consists of 1000 accident clips each of which is 5-6 seconds in length. For preprocessing, the following steps have been followed.

1) The non-accident frames of each clip is extracted and are transformed into matrix in the batches of 10. Each batch represents a sequence.
2) These batches are then fed into the model for training, the input and output of the autoencoder is kept same in order to teach the model to generate non-accidents frame, after which we use this model for prediction purpose.
3) For prediction, the accident frames from the video is fed and in the output we get frames generated by the model.
4) There is a huge reconstruction loss when we give accident frames to the model and hence we can say accident has occured.

Given below is a visualization of above mentioned points.

![viz](https://github.com/pradyyadav/Images/blob/main/trainae.png?raw=true)

## Technologies

- #### Languages and Frameworks
  Python
- #### Libraries
  Matplotlib
  
  OpenCV
  
  Tensorflow
