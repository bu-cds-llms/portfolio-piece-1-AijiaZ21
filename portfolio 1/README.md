# Neural Network Exploration: Learning XOR

## Overview
This portfolio explores how neural network architecture and hyperparameters affect learning on the XOR problem. XOR is a classic example of a non-linearly separable task, which makes it useful for understanding why hidden layers and non-linear activation functions are necessary in neural networks. 

Through controlled experiments, I analyze how model depth, activation function choice, and learning rate influence training behavior.


## Methods
I implemented a fully connected neural network in PyTorch. The architecture is configurable so that I can vary:

- Number of hidden layers  
- Hidden layer size  
- Activation function (ReLU or Tanh)  
- Learning rate  

The output layer produces logits, and I use `BCEWithLogitsLoss` for binary classification.  
Models are trained using stochastic gradient descent (SGD), and I record the training loss over time to visualize optimization behavior.

I conducted controlled experiments where I varied:
1. Model depth (1 vs 2 hidden layers)
2. Activation function (ReLU vs Tanh)
3. Learning rate (0.1 vs 1.0)

All other factors were kept constant.


## Key Results
- A network with only one hidden layer struggled to effectively reduce loss.
- Increasing depth to two hidden layers allowed the model to successfully learn XOR.
- Both ReLU and Tanh activation functions solved the task, though their convergence patterns differed slightly.
- A higher learning rate (1.0) led to much faster convergence, but may cause instability in more complex settings.

These experiments demonstrate how architectural and optimization choices directly affect learning dynamics.


## How to Run

### Run in Google Colab

1. Go to the GitHub repository:  
   `portfolio-piece-1-AijiaZ21`

2. Download the file `portfolio_1.ipynb`.

3. Open Google Colab:  
   https://colab.research.google.com/

4. Upload `portfolio_1.ipynb`.

5. Run all cells to reproduce the experiments and visualizations.


## Requirements

This project requires the following packages:

- Python 3.9+
- PyTorch
- matplotlib

If running in Google Colab, most dependencies are already pre-installed. 
