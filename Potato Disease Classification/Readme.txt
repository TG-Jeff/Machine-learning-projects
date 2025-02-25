
# Potato Disease Classification using CNN

## Overview
This project aims to classify potato leaf images into three categories:
1. **Potato___Late_blight**: Leaves affected by late blight disease.
2. **Potato___Early_blight**: Leaves affected by early blight disease.
3. **Potato___healthy**: Healthy potato leaves.

The project uses a **Convolutional Neural Network (CNN)** built with TensorFlow and Keras to automatically detect and classify potato diseases based on leaf images. This can help farmers identify diseases early and take appropriate action to protect their crops.

---

## Dataset
The dataset used in this project is available on [Kaggle](https://www.kaggle.com/faysalmiah1721758/potato-dataset). It contains:
- **2152 images** of potato leaves.
- Three classes:
  - `Potato___Late_blight`: 1000 images.
  - `Potato___Early_blight`: 1000 images.
  - `Potato___healthy`: 152 images.

The dataset is split into:
- **Training set**: 80% of the data.
- **Validation set**: 20% of the data.

---

## Model Architecture
The CNN model consists of the following layers:
1. **Convolutional Layers**:
   - Four convolutional layers with ReLU activation.
   - Max-pooling layers to reduce spatial dimensions.
2. **Fully Connected Layers**:
   - Two Dense layers with 128,64 units respectively and ReLU activation.
   - Dropout layer (50%) to prevent overfitting.
3. **Output Layer**:
   - A dense layer with 3 units (one for each class) and softmax activation.

The model is compiled using:
- **Optimizer**: Adam.
- **Loss Function**: Categorical cross-entropy.
- **Metrics**: Accuracy.

---

## Results
The model achieves the following performance:
- **Training Accuracy**: ~94.57%.
- **Validation Accuracy**: ~96.51%.
- **Validation Loss**: ~0.1067.

Early stopping was used to prevent overfitting, and the best model weights were restored at epoch 13.

---

