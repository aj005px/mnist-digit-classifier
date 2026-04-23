# mnist-digit-classifier

A beginner-friendly handwritten digit classifier built with TensorFlow and Keras. Trains a simple feedforward neural network on the MNIST dataset to recognize digits (0–9), evaluates its accuracy on unseen data, and visualizes prediction quality using a confusion matrix heatmap.

---

## 🧠 What it does

1. **Loads the MNIST dataset** — 60,000 training images and 10,000 test images of handwritten digits, sourced directly from `keras.datasets`.
2. **Preprocesses the data** — Normalizes pixel values to the `[0, 1]` range and flattens each 28×28 image into a 784-dimensional vector.
3. **Trains a neural network** — A single Dense layer with 10 neurons (one per digit class), sigmoid activation, and the Adam optimizer, trained for 5 epochs using sparse categorical cross-entropy loss.
4. **Evaluates performance** — Reports loss and accuracy on the held-out test set.
5. **Visualizes predictions** — Renders a confusion matrix heatmap using Seaborn to show where the model succeeds and where it makes mistakes.

---

## 🗂️ Project Structure

```
mnist-digit-classifier/
├── tensorflow.ipynb   # Main notebook — training, evaluation, and visualization
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation

```bash
pip install tensorflow numpy matplotlib seaborn
```

### Run

```bash
jupyter notebook tensorflow.ipynb
```

Run all cells from top to bottom. The MNIST dataset will be downloaded automatically on first run.

---

## 📊 Model Architecture

| Layer | Type  | Units | Activation |
|-------|-------|-------|------------|
| 1     | Dense | 10    | Sigmoid    |

- **Optimizer:** Adam  
- **Loss:** Sparse Categorical Cross-Entropy  
- **Epochs:** 5  
- **Input shape:** `(784,)` (flattened 28×28 image)

---

## 📈 Results

After 5 epochs, the model typically achieves ~92% accuracy on the test set. The confusion matrix reveals which digit pairs are most commonly confused (e.g., 4 vs 9, 3 vs 5).

---

## 🔧 Potential Improvements

- Add hidden layers with ReLU activations for better accuracy
- Use `Conv2D` layers (CNN) to exploit spatial structure in images
- Increase training epochs with early stopping
- Add dropout regularization to reduce overfitting

---

## 📚 References

- [TensorFlow Documentation](https://www.tensorflow.org/)
- [Keras MNIST Dataset](https://keras.io/api/datasets/mnist/)
- [MNIST Database](http://yann.lecun.com/exdb/mnist/)
