# ERA-S5
### Assignment for ERA Session 5: Re-structuring the code

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/release/python-380/)

### Source Files
- `model.py` This file contains the Architecture of Neural Network developed for MNIST dataset with PyTorch.
- `utils.py` This file contains utility functions required for model training, evaluation, plotting results etc.
- `S5.ipynb` This is out main notebook where we perform our experiments with MNIST dataset and the defined model.

### Usage
 1. Import required modules in S5.ipynb notebook, including `torch`, `torchvision` and other submodules
 2. Import NeuralNet model `Net` class from `model.py`
 3 Import training functions, helper functions for plotting etc from `utils.py`
 4 Start with image transformation using `torchvision.transforms`
 5 Download the MNIST data and create a dataset out of it, using `torchvision.datasets`
 6 Create both training and testing dataloaders with required number of batches
 7 Define **loss function, optimizer, learning rate, scheduler, epochs** with preferred hyper paramters
 8 Start the model training and accumulate the losses and accuracy values for both training and testing phases
 9 Once training is completed, evaluate the losses and accuracy values collected during the training using plot_results function
 10 We can also check the internals of the model using `summary` function from `torchinfo` module *(Added sample below)*

