# MNIST Digit Classification using Neural Networks and CNN

This project demonstrates a step-by-step approach to improve the accuracy of digit classification using the MNIST dataset, starting from a basic neural network to a CNN-enhanced model.

---

## 📊 Dataset

- **MNIST Dataset**: 70,000 grayscale images of handwritten digits (28x28 pixels).
- Split:
  - 80% Training
  - 10% Validation
  - 10% Testing

---

## 🧪 Models & Results

### 1. Basic Neural Network (No Hidden Layers)
- **Architecture**: Single dense output layer with sigmoid activation.
- **Accuracy**: `93.75%`

---

### 2. Neural Network with Hidden Layers
- **Architecture**:
  - Dense (100 units) + PReLU
  - Dense (50 units) + PReLU
  - Dense (25 units) + PReLU
  - Output Dense (10 units) with softmax
- **Accuracy**: `98.22%`

---

### 3. Flatten Layer + Hidden Layers
- **Architecture**:
  - Flatten Input (28x28)
  - Dense (100) + PReLU
  - Dense (50) + PReLU
  - Output Dense (10) with sigmoid
- **Accuracy**: `97.75%`

---

### 4. CNN + Flatten + Hidden Layers
- **Architecture**:
  - Conv2D (64 filters, 4x4) + ReLU + MaxPooling (3x3)
  - Conv2D (32 filters, 3x3) + ReLU + MaxPooling (2x2)
  - Flatten
  - Dense (100) + ReLU
  - Dense (50) + ReLU
  - Dense (25) + ReLU
  - Output Dense (10) with softmax
- **Accuracy**: `99.27%`

---

## ⚙️ Training Details

- **Optimizer**: Adadelta with learning rate = 1.0
- **Loss Function**: Sparse Categorical Crossentropy
- **Epochs**: 25 (10 for one model)
- **Activation Functions**:  Sigmoid, Softmax, ReLU

---

## ✅ Summary

| Model Type                  | Accuracy |
|----------------------------|----------|
| No Hidden Layer            | 93.75%   |
| Hidden Layers (Dense)      | 98.22%   |
| Flatten + Hidden Layers    | 97.75%   |
| CNN + Flatten + Hidden     | 99.27%   |

Progressively increasing model complexity improved accuracy from **93.75% to 99.27%**.

---
