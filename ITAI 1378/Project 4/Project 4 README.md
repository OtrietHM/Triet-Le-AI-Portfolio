## 🧠 Deep Learning for Image Classification (Fashion-MNIST)

This project implements a Convolutional Neural Network (CNN) to classify images from the **Fashion-MNIST dataset**, demonstrating a complete deep learning workflow, effective feature learning, and strong generalization.

---

### Problem Statement: What problem does this solve?

The project aims to achieve **reliable image classification** for 10 clothing categories from 28x28 grayscale images by implementing an efficient deep learning model that automatically learns visual features.

### Approach: How did you solve it? What methods/algorithms?

The approach uses a CNN architecture built with TensorFlow/Keras.

1.  **Data Preprocessing:** Images were **normalized** (scaled 0-1) and **reshaped** (28, 28, 1). Labels were **one-hot encoded**.
2.  **Model Architecture:** A CNN was constructed using:
    - **Convolutional Layers (`Conv2D`):** Automatically learned features (e.g., edges and textures).
    - **ReLU Activation:** Used in hidden layers.
    - **Pooling (`MaxPool2D`):** Reduced feature map dimensionality and complexity.
    - **Softmax Output:** Used for final 10-class probability prediction.
3.  **Optimization:** Trained using the **Adam optimizer** and **Categorical Cross-Entropy** loss.

### Results: What were your results? Include metrics, accuracy, performance

The model successfully learned the patterns with high accuracy and minimal overfitting:

| Metric                  | Value      |
| :---------------------- | :--------- |
| **Final Test Accuracy** | **91.13%** |
| Final Test Loss         | 0.2520     |

- **Performance:** Training and validation loss/accuracy curves tracked closely, indicating **good generalization**.
- **Primary Errors:** Misclassifications were concentrated between visually ambiguous items, such as **Pullover (ID 2)** and **Shirt (ID 6)**.

### Key Findings: What did you learn from this project?

- **Automatic Feature Learning:** CNNs successfully **bypass manual feature engineering** (e.g., HOG/LBP), automatically learning hierarchical and complex features directly from pixel data.
- **Generalization:** The model demonstrated strong generalization with a small performance gap between training and validation, confirming it **learned patterns effectively**.

### Technologies Used

- **TensorFlow/Keras**
- **Python, NumPy, Matplotlib**

### How to Run: Brief instructions

1.  Open the `L04_NhaHuynh_ITAI_1378.ipynb` notebook in **Google Colab**.
2.  Run all cells sequentially to train and evaluate the CNN.
