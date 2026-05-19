# Rock Paper Scissors Classification using CNN

A Deep Learning project for classifying hand gestures into:

- Rock
- Paper
- Scissors

using a Convolutional Neural Network (CNN) implemented with PyTorch.

---

# Project Overview

This project uses a CNN model to classify images of hand gestures from the Rock-Paper-Scissors dataset.

The project includes:

- Data preprocessing
- Data augmentation
- CNN architecture design
- Model training and evaluation
- Adam vs SGD comparison
- Early stopping
- Visualization and performance analysis

---

# Dataset

Dataset Classes:

- Paper
- Rock
- Scissors

Dataset Size:
- ~2900 images

Dataset Source:
- TensorFlow Rock Paper Scissors Dataset

---

# Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Scikit-learn

---

# Data Preprocessing

The following preprocessing techniques were applied:

```python
transforms.Resize((128,128))

transforms.RandomHorizontalFlip()

transforms.RandomRotation(10)

transforms.ColorJitter(
    brightness=0.2,
    contrast=0.2
)

transforms.ToTensor()

transforms.Normalize(
    [0.5,0.5,0.5],
    [0.5,0.5,0.5]
)
```

---

# CNN Architecture

The model consists of:

- Convolution Layers
- Batch Normalization
- ReLU Activation
- MaxPooling
- Dropout
- Fully Connected Layers

Architecture Summary:

```python
Conv2D → BatchNorm → ReLU → MaxPool
Conv2D → BatchNorm → ReLU → MaxPool
Conv2D → BatchNorm → ReLU → MaxPool
Flatten
Linear
Dropout
Linear
```

---

# Optimizers Comparison

Two optimizers were tested:

| Optimizer | Best Validation Accuracy |
|---|---|
| Adam | 99.74% |
| SGD | 99.74% |

Observation:

- Adam converged faster during early epochs.
- SGD required more epochs to achieve similar performance.

---

# Techniques Used to Reduce Overfitting

- Data Augmentation
- Batch Normalization
- Dropout
- Early Stopping

---

# Training Configuration

| Parameter | Value |
|---|---|
| Image Size | 128x128 |
| Batch Size | 32 |
| Epochs | 15 |
| Loss Function | CrossEntropyLoss |
| Optimizers | Adam / SGD |

---

# Results

## Classification Report

```text
              precision    recall  f1-score   support

       paper       1.00      0.99      1.00
        rock       1.00      1.00      1.00
    scissors       0.99      1.00      1.00
```

Final Validation Accuracy:

```text
99.74%
```

---

# Project Structure

```text
project/
│
├── dataset/
│
├── models/
│   ├── best_model.pth
│   └── best_model_sgd.pth
│
├── results/
│   ├── accuracy_graph.png
│   ├── confusion_matrix.png
│   └── predictions.png
│
├── notebook.ipynb
│
└── README.md
```

---




## Run Notebook

Open:

```text
notebook.ipynb
```

using:
- Jupyter Notebook
- Google Colab

# Conclusion

This project demonstrates how CNNs can achieve high accuracy in image classification tasks using proper preprocessing, regularization, and optimization techniques.
