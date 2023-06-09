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
 3. Import training functions, helper functions for plotting etc from `utils.py`
 4. Start with image transformation using `torchvision.transforms`
 5. Download the MNIST data and create a dataset out of it, using `torchvision.datasets`
 6. Create both training and testing dataloaders with required number of batches
 7. Define **loss function, optimizer, learning rate, scheduler, epochs** with preferred hyper paramters
 8. Start the model training and accumulate the losses and accuracy values for both training and testing phases
 9. Once training is completed, evaluate the losses and accuracy values collected during the training using plot_results function
 10. We can also check the internals of the model using `summary` function from `torchinfo` module *(Added sample below)*

## Sample Images from Train dataset
![image](https://github.com/RaviNaik/ERA-S5/assets/23289802/13e1d013-a37b-4c9b-a25d-0bd1269f4d83)

## Training Results
![image](https://github.com/RaviNaik/ERA-S5/assets/23289802/3117ad03-fad7-49bd-8c48-b72890913dbf)

## Model Summary
```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 32, 26, 26]             288
            Conv2d-2           [-1, 64, 24, 24]          18,432
            Conv2d-3          [-1, 128, 10, 10]          73,728
            Conv2d-4            [-1, 256, 8, 8]         294,912
            Linear-5                   [-1, 50]         204,800
            Linear-6                   [-1, 10]             500
================================================================
Total params: 592,660
Trainable params: 592,660
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.67
Params size (MB): 2.26
Estimated Total Size (MB): 2.93
----------------------------------------------------------------
```


