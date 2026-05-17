# Rock Paper Scissors Classification using CNN

A Deep Learning project for classifying hand gesture images into three classes: Rock, Paper, and Scissors using a Convolutional Neural Network (CNN) built with PyTorch.

## Dataset
- Dataset: Rock Paper Scissors
- Source: TensorFlow Datasets (`tensorflow_datasets`)
- Classes:
  - Rock
  - Paper
  - Scissors

## Project Objective
Build and evaluate a CNN model for image classification and compare two experiments with different hyperparameters.

## Experiments

| Experiment | Configuration | Best Test Accuracy |
|----------|----------|----------|
| Experiment 1 | Adam, Learning Rate = 0.001, Dropout = 0.5 | 98.92% |
| Experiment 2 | Adam, Learning Rate = 0.0005, Dropout = 0.3, Weight Decay = 1e-4 | 92.74% |

## Model Architecture
- Convolutional Layers
- Batch Normalization
- Max Pooling
- Fully Connected Layers
- Dropout

## Training Details
- Framework: PyTorch
- Loss Function: Cross Entropy Loss
- Optimizer: Adam
- Early Stopping
- Best Model Saving

## Evaluation Metrics
- Accuracy
- Loss
- Confusion Matrix
- Classification Report

## Visualizations
- Training vs Validation Accuracy
- Training vs Validation Loss
- Sample Predictions

## Requirements

```bash
pip install torch torchvision tensorflow-datasets matplotlib numpy scikit-learn
