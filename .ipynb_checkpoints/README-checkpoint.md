# Amazigh Alphabets Recognition

This project implements a deep learning model using TensorFlow and Keras to accurately recognize Amazigh alphabet characters from images.
The trained model can predict characters from user-supplied images.

## Contents

- **`Amazigh-Alphabets-Recognition.ipynb`**: Jupyter Notebook for training the model, visualizing its performance, and saving it.
- **`Test_Amazigh-Alphabets-Model.ipynb`**: Python script to load the saved model and make predictions on new images.
- **`test_images`**: Directory to store user-provided images for prediction.
- **`amazigh_alphabets_model.keras`**: Saved model file containing the trained neural network weights and architecture.

## Model Architecture

The model architecture consists of:
- **Input Layer**: Conv2D layer with ReLU activation for processing 68x68 RGB images.
- **First Convolutional Layer**: 6 filters with 5x5 kernels, followed by MaxPooling.
- **Second Convolutional Layer**: 16 filters with 5x5 kernels, followed by MaxPooling.
- **Flatten Layer**: Converts the 2D feature maps to a 1D vector.
- **Fully Connected Layers**: Dense layers with 120 and 84 units, using ReLU activation.
- **Output Layer**: Dense layer with 33 units and softmax activation for multi-class classification (one unit per Amazigh character).

Open `Amazigh-Alphabets-Recognition.ipynb` in Jupyter Notebook if you want to add some hidden layer or change the architecture, run all cells to train the model, evaluate its performance, and save it as `amazigh_alphabets_model.keras`.

## Making Predictions

To make predictions on new images:
1. Place your images in the `test_images/` folder. Ensure that the images are in PNG format and named appropriately.
2. Run the `Test_Amazigh-Alphabets-Model.ipynb` script. This script will:
   - Load the saved model from `amazigh_alphabets_model.keras`.
   - Process the images in the `test_images/` folder.
   - Display the predictions along with the input images.
