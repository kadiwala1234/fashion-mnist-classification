[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Cadno_xnAMXWQrche1-7GhbC0__FXGEv?usp=sharing)
# Image Classification using Feedforward Neural Networks (Fashion MNIST)

## Project Overview

This project demonstrates the application of a **feedforward neural network (FNN)** for image classification using the Fashion MNIST dataset. The goal is to classify grayscale images of clothing items into one of 10 categories and evaluate the effectiveness of deep learning compared to traditional machine learning approaches.

## Dataset

The project uses the **Fashion MNIST** dataset, which contains:

* 70,000 grayscale images (28×28 pixels)
* 10 clothing categories:

  * T-shirt/top
  * Trouser
  * Pullover
  * Dress
  * Coat
  * Sandal
  * Shirt
  * Sneaker
  * Bag
  * Ankle boot

Dataset split:

* 60,000 training images
* 10,000 test images

Source: Zalando Research (via TensorFlow/Keras)

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Model Architecture

The neural network consists of:

* **Input Layer:** 784 neurons (flattened 28×28 image)
* **Hidden Layer 1:** 128 neurons (ReLU activation)
* **Dropout Layer:** 30% (reduces overfitting)
* **Hidden Layer 2:** 64 neurons (ReLU activation)
* **Output Layer:** 10 neurons (Softmax activation)

## Methodology

### 1. Data Preprocessing

* Normalized pixel values to range [0, 1]
* Flattened images into 1D vectors
* Applied one-hot encoding to labels

### 2. Model Training

* Optimizer: Adam
* Loss Function: Categorical Crossentropy
* Batch Size: 32
* Epochs: 15
* Validation Split: 20%

### 3. Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

## Results

* **Test Accuracy:** ~85–88%
* Model performs well on distinct categories like *Bag* and *Ankle boot*
* Misclassifications occur between visually similar classes such as *Shirt* and *T-shirt/top*

### Key Observations

* Training accuracy improves steadily across epochs
* Slight overfitting observed in later epochs
* Dropout helps improve generalization

## Visualizations Included

* Training vs Validation Accuracy graph
* Training vs Validation Loss graph
* Confusion Matrix heatmap
* Sample dataset images

## Model Improvements

An enhanced model was also tested with:

* Additional hidden layers
* Increased neurons (256 → 128 → 64)
* Higher dropout rates

This resulted in improved generalization and slightly higher accuracy.

## Real-World Applications

This model can be applied in:

* **Fashion Retail** – automatic product categorization
* **Image Organization** – tagging and sorting images
* **E-commerce** – recommendation systems

## Limitations

* Feedforward networks ignore spatial relationships in images
* Lower performance compared to Convolutional Neural Networks (CNNs)
* Not ideal for complex, high-resolution datasets

## Future Improvements

* Implement Convolutional Neural Networks (CNNs)
* Apply data augmentation techniques
* Use transfer learning for better accuracy
* Deploy model using a web application

## How to Run the Project

### Option 1: Google Colab

1. Open the notebook in Google Colab
2. Run all cells sequentially

### Option 2: Local Environment

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
```

Run the notebook:

```bash
jupyter notebook
```

## Project Structure

```
├── notebook.ipynb        # Main implementation
├── README.md             # Project documentation
├── report.pdf            # Final report
└── images/               # Saved visualizations (optional)
```

## Submission Details

* Google Colab Notebook
* GitHub Repository
* PDF Report

## Key Insight

While feedforward neural networks perform reasonably well, **Convolutional Neural Networks (CNNs)** are significantly more effective for image classification tasks because they preserve spatial information.

## License

This project is for academic purposes only.
