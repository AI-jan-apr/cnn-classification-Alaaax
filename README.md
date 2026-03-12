# CNN Image Classification — Cats vs Dogs

## Overview
This project builds a Convolutional Neural Network (CNN) to classify images into two categories: Cats and Dogs.
The full computer vision pipeline was implemented including data preprocessing, model training, evaluation, and performance analysis.

---

# Dataset
The dataset used for this task is **Dogs vs. Cats**:

[Kaggle Dataset - Dog vs. Cat](https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset/data)


Classes:
- Cat
- Dog

Dataset split:

| Split | Images |
|------|------|
| Training | 17,498 |
| Validation | 3,750 |
| Test | 3,750 |

---

# Project Steps

## 1. Data Cleaning
The dataset was first checked for corrupted or unreadable images.
Invalid images were removed to prevent training errors.

## 2. Data Splitting
The dataset was divided into:
- Training set
- Validation set
- Test set

This ensures the model is evaluated on unseen data.

## 3. Data Preprocessing
Images were normalized by converting pixel values from 0–255 to 0–1.

### Data Augmentation
To improve generalization, augmentation techniques were applied:
- Rotation
- Zoom
- Horizontal Flip

---

# CNN Model Architecture
The CNN model includes:
- Convolution layers
- MaxPooling layers
- Flatten layer
- Dense layer
- Dropout layer

CNNs automatically learn visual features such as edges, textures, and shapes.

---

# Initial Model Results
Before improvements:

Accuracy: 0.8536  
Loss: 0.3573

---

# Model Improvement
Two improvements were applied:

1. Increase epochs from 10 to 20
2. Add EarlyStopping to stop training when validation loss stops improving

---

# Final Model Results

Test Accuracy: 0.91  
Test Loss: 0.2122

| Metric | Before | After |
|------|------|------|
| Accuracy | 0.8536 | 0.91 |
| Loss | 0.3573 | 0.2122 |

---

# Training Performance Visualization

Training vs Validation Accuracy shows that both curves improved steadily with a small gap between them, indicating good generalization.

Training vs Validation Loss shows a steady decrease, indicating stable model learning.

---

# Confusion Matrix

| True Class | Predicted Cat | Predicted Dog |
|------|------|------|
| Cat | 1726 | 149 |
| Dog | 162 | 1713 |

This shows the model correctly classified most images in both classes.

---

# Additional Metrics

Precision: 0.79  
Recall: 0.95  
F1-score: 0.86  

These metrics confirm strong classification performance.

---

# Findings

Final Accuracy: 0.91  
Final Loss: 0.2122  

The CNN model achieved strong performance on the cats vs dogs classification task.
Initially the model achieved an accuracy of 0.8536 with a loss of 0.3573.

After increasing the number of epochs and introducing EarlyStopping, the model performance improved significantly to 0.91 accuracy and 0.2122 loss.

This shows that adjusting the training strategy allowed the model to learn better visual features while preventing overfitting.
