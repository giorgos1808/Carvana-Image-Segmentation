# Carvana Image Segmentation Project

This repository contains code for a project focused on image segmentation using various U-Net architectures on the Carvana dataset. The project includes implementations of U-Net models with different encoders such as vanilla U-Net, VGG-13, VGG-16, ResNet-18, ResNet-34, and ResNet-50.

## Files:

### 1. `dataset.py`

The `dataset.py` file defines the `CarvanaDataset` class, which is a PyTorch `Dataset` for loading images and their corresponding masks. This class is crucial for organizing and handling the dataset used for training and evaluation.

### 2. `unet.py`

This file defines the U-Net architecture, which is the baseline model for image segmentation. The U-Net consists of an encoding path followed by a decoding path, with skip connections to retain spatial information.

### 3. `vgg_unet.py`

This file contains implementations of U-Net models with VGG-13 and VGG-16 encoders. These models leverage the pre-trained VGG models from torchvision and integrate them into the U-Net architecture.

### 4. `resnet_unet.py`

This file provides U-Net models with ResNet-18, ResNet-34, and ResNet-50 encoders. Similar to the VGG models, these implementations use pre-trained ResNet models and combine them with the U-Net structure for image segmentation.

### 5. `train.py`

The `train.py` script is the main training and evaluation script. It includes the training loop, data transformations, model setup, hyperparameters, and the main function to train and evaluate U-Net models on the Carvana dataset.

### 6. `utils.py`

This utility file includes functions for loading and saving checkpoints, calculating accuracy, and saving predictions as images. These functions are used in the training script to enhance code modularity.

### 7. `ptorch.yml`

The `ptorch.yml` file contains a YAML configuration for managing project dependencies. You can use this file to create a conda environment or install the required packages using:

## Usage:

To run the project, follow these steps:

1. Install the required dependencies:

   ```bash
   conda env create -f ptorch.yml
   conda activate ptorch
