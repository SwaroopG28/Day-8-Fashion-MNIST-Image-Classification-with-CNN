## **Day 8: Fashion MNIST Image Classification with CNN**

### 📄 **Project Overview**
This project demonstrates how to classify images of clothing items from the **Fashion MNIST dataset** using a **Convolutional Neural Network (CNN)**. The CNN learns spatial hierarchies of features through convolutional and pooling layers, making it well-suited for image data.

**Dataset Link:** [Fashion MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist)

---

### 🎯 **Objective**
- Build and train a **CNN** to classify clothing images into one of 10 categories.
- Evaluate the model on unseen test data and visualize the results.

---

### 📊 **Dataset Description**
- **Images:** 70,000 grayscale images (28x28 pixels) representing 10 categories of clothing items.
- **Training Data:** 60,000 images.
- **Testing Data:** 10,000 images.
- **Classes:**
  1. T-shirt/top
  2. Trouser
  3. Pullover
  4. Dress
  5. Coat
  6. Sandal
  7. Shirt
  8. Sneaker
  9. Bag
  10. Ankle boot

---

### ⚙️ **Technologies Used**
- **TensorFlow/Keras:** For building and training the CNN.
- **NumPy:** For numerical computations.
- **Matplotlib:** For data visualization.

---

### 🛠️ **Steps Performed**

#### 1. **Data Preprocessing**
- Normalized pixel values to the range `[0, 1]` to improve training efficiency.
- Reshaped images to include a channel dimension for compatibility with CNNs.
- One-hot encoded the target labels for multi-class classification.

#### 2. **CNN Architecture**
- **Convolutional Layers:** Extracted spatial features using filters.
- **MaxPooling Layers:** Reduced spatial dimensions while retaining essential information.
- **Dropout Layers:** Regularized the model to prevent overfitting.
- **Dense Layers:** Fully connected layers for classification.
- **Output Layer:** Used a softmax activation function to produce probabilities for each class.

#### 3. **Compilation**
- **Optimizer:** Adam optimizer to minimize the loss function effectively.
- **Loss Function:** Categorical crossentropy for multi-class classification.
- **Metric:** Accuracy to evaluate model performance.

#### 4. **Model Training**
- Trained the model for 10 epochs with a batch size of 64.
- Used 20% of the training data for validation.

#### 5. **Evaluation and Visualization**
- Evaluated the model on the test set and achieved high accuracy.
- Plotted training/validation accuracy and loss to monitor model performance.
- Visualized predictions on test images along with their true labels.

#### 6. **Model Saving**
- Saved the trained model as `fashion_mnist_cnn_model.h5` for reuse.

---

### 📈 **Results**
- **Test Accuracy:** Achieved a high classification accuracy on unseen test data.
- **Visualizations:**
  - Training and validation accuracy/loss curves.
  - Sample test predictions with true and predicted labels.
