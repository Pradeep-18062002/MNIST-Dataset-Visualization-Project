MNIST Dataset Visualization Project

Objective:


The goal of this project is to load the MNIST dataset, which consists of handwritten digit images (0–9), and visualize one example of each digit by:

1) Loading the dataset into matrices Xraw (features) and Yraw (labels).
2) Selecting one image for each digit (0 through 9).
3) Reshaping the selected images from a flat format (784 pixels) to their original 28×28 grid structure.
4) Plotting the reshaped images to visualize the handwritten digits.


Dataset Details:

Source: MNIST dataset (can be loaded via sklearn or similar libraries).

Features (Xraw):
Contains 70,000 rows, each with 784 pixel values (28×28 flattened grid).
Pixel values range from 0 (black) to 255 (white).

Labels (Yraw):
Contains 70,000 rows, each corresponding to the digit label (0–9).
