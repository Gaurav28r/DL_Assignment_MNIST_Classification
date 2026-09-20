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

## Visualizations & Outputs

### 1. Sample Data
<img width="446" height="482" alt="Screenshot 2026-09-20 190511" src="https://github.com/user-attachments/assets/311262a1-6a96-4990-a87f-e700d2938959" />

### 2. Model Architecture
<img width="662" height="312" alt="Screenshot 2026-09-20 190605" src="https://github.com/user-attachments/assets/64b65a30-7aa9-43ba-8129-a598740237be" />


### 3. Model Training Curves
**Training vs. Validation Accuracy**
<img width="872" height="507" alt="Screenshot 2026-09-20 190724" src="https://github.com/user-attachments/assets/40cf6a7e-80ca-4701-998d-34cdee298c69" />


**Training vs. Validation Loss**
<img width="862" height="523" alt="Screenshot 2026-09-20 190826" src="https://github.com/user-attachments/assets/47347b40-1c7b-42bc-b86f-1bf78a83b132" />



### 4. Prediction on Test Images
<img width="1662" height="408" alt="Screenshot 2026-09-20 190916" src="https://github.com/user-attachments/assets/f3bce098-080b-4e93-b7c9-ea8330bccd13" />


## Results & Comparison
Both models performed exceptionally well on the test dataset. The experimental model with increased neurons showed a slight improvement in overall accuracy and a reduction in test loss.

<img width="386" height="121" alt="Screenshot 2026-09-21 000248" src="https://github.com/user-attachments/assets/aabdfe12-7c01-4995-8063-c514580973df" />


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
