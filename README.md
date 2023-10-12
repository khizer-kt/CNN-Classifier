# CNN-Classifier  
Binary Image Classification on Custom Dataset using Convolutional Neural Networks  

This code is a Python script that demonstrates the process of building a simple Convolutional Neural Network (CNN) using TensorFlow and Keras for binary image classification. Here's a description of the key components and steps:

### Data Preparation:

The script begins by specifying a data_dir directory, where it assumes image data is stored. It also defines a list of valid image extensions (e.g., jpeg, jpg, bmp, png).

It then iterates through the directories inside data_dir, checks each image in those directories for validity based on their extensions, and removes any invalid images.

### Data Loading:

TensorFlow's image_dataset_from_directory is used to load the image data from the data directory into a dataset. It prints the number of files found and the number of classes.
### Data Augmentation:

Data augmentation is performed using ImageDataGenerator to rescale pixel values and create training and validation data splits. It sets aside 20% of the data for validation.
### Model Definition:

A simple CNN model is defined using Keras Sequential API. It consists of two convolutional layers with max-pooling, followed by two fully connected layers. The final output layer has one neuron for binary classification (happy or sad).
### Model Compilation:

The model is compiled with the Adam optimizer, binary cross-entropy loss, and accuracy as the evaluation metric.
### Model Training:

The model is trained using the fit method. It runs for 10 epochs and uses the training and validation datasets. The training progress and performance metrics (loss and accuracy) are displayed for each epoch.
### Plotting Training History:

Matplotlib is used to visualize the training history, plotting the training and validation accuracy across epochs.
### Model Saving:

The trained model is saved as 'happysad.h5' using Keras' model.save method.
### Model Loading and Testing:

The saved model is loaded from the 'happysad.h5' file.

An image is loaded from 'test.png' for testing. It is preprocessed to match the model's input size.
The loaded model is used to make a prediction on the test image, and the result (happy or sad) is displayed with a corresponding image using Matplotlib.
