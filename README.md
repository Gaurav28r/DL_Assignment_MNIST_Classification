# MNIST Handwritten Digit Classification using Deep Learning

## Overview
This project implements a feedforward neural network using TensorFlow and Keras to classify handwritten digits (0-9) from the MNIST dataset. It was developed as part of a Deep Learning academic assignment to demonstrate dataset exploration, model design, evaluation, and architectural experimentation.

## Project Deliverables
* **Jupyter Notebook:** Contains the full Python code for the implementation.
* **Handwritten Report:** A detailed 2-3 page report covering the methodology, neural network background, and conclusions.

## Methodology & Steps
1. **Dataset Loading & Exploration:** The MNIST dataset (60,000 training images and 10,000 testing images of 28x28 pixels) is loaded and explored. 
2. **Data Preprocessing:** Grayscale pixel values are normalized from 0-255 to a 0-1 float range.
3. **Baseline Model Design:** A simple neural network is built with a `Flatten` layer, two hidden `Dense` layers (128 and 32 neurons) using ReLU activation, and a 10-neuron output layer using Softmax activation.
4. **Compilation & Training:** The model is compiled using the Adam optimizer and `sparse_categorical_crossentropy` loss. It is trained over 25 epochs with a 20% validation split.
5. **Evaluation & Visualization:** The model is evaluated on the test set. Training and validation accuracy, along with loss, are visualized using Matplotlib.
6. **5-Image Prediction Test:** The trained model is tested on 5 individual handwritten images, comparing actual labels against the model's predictions.
7. **Architectural Experimentation:** An experimental model is created by increasing the hidden layer neurons from (128, 32) to (256, 64) to compare performance.

## Results & Comparison
Both models performed exceptionally well on the test dataset. The experimental model with increased neurons showed a slight improvement in overall accuracy and a reduction in test loss.

| Model | Hidden Layers | Epochs | Test Accuracy | Test Loss |
| :--- | :--- | :--- | :--- | :--- |
| **Baseline** | 128, 32 | 25 | 96.27% | 0.1284 |
| **Experimental** | 256, 64 | 25 | 97.31% | 0.0903 |

*Difference in Test Accuracy: +1.04%*

## Dependencies
To run the notebook, you will need the following Python libraries installed:
* `tensorflow` / `keras`
* `numpy`
* `pandas`
* `matplotlib`

## How to Run
1. Clone the repository.
2. Open the Jupyter Notebook (`.ipynb`) in Google Colab or a local Jupyter environment.
3. Run all cells sequentially to download the dataset, train the models, and generate the plots and predictions.
