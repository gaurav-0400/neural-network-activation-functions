# Neural Network From Scratch

A beginner-friendly implementation of a simple neural network built from scratch using **Python and NumPy**.

This project is designed to understand the fundamental workflow of neural networks without directly relying on high-level deep learning frameworks.

The project demonstrates how a neural network learns through:

**Perceptron → Weights & Bias → Activation Function → Forward Propagation → Loss Function → Backward Propagation → Gradient Descent → Training → Prediction**

---

## 📌 Project Overview

In this project, we build a simple binary classification model to predict whether a student will **Pass or Fail** based on:

- Study Hours
- Attendance

The model uses:

- NumPy for numerical computations
- Sigmoid activation function
- Binary Cross Entropy loss
- Backward propagation
- Gradient Descent
- Matplotlib for training visualization

The main purpose of this project is **learning and understanding the internal workflow of a neural network**.

---

## 🧠 Concepts Covered

This project covers the following concepts step by step:

1. Dataset creation
2. Input features and target
3. Data normalization
4. Weights
5. Bias
6. Perceptron
7. Weighted sum
8. Sigmoid activation function
9. Forward propagation
10. Prediction
11. Binary Cross Entropy loss
12. Backward propagation
13. Gradient calculation
14. Gradient Descent
15. Weight and bias updates
16. Epochs and training
17. Loss visualization
18. Model evaluation
19. Prediction on new data

---

## 🔄 Neural Network Workflow

```text
Input Data
    ↓
Normalization
    ↓
Initialize Weights & Bias
    ↓
Weighted Sum
    ↓
Activation Function
    ↓
Forward Propagation
    ↓
Prediction
    ↓
Loss Function
    ↓
Backward Propagation
    ↓
Calculate Gradients
    ↓
Gradient Descent
    ↓
Update Weights & Bias
    ↓
Repeat for Multiple Epochs
    ↓
Final Prediction
```

---

## 📂 Project Structure

```text
neural-network-from-scratch/
│
├── neural_network_from_scratch.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

### Files

**`neural_network_from_scratch.ipynb`**

Contains the complete implementation with step-by-step explanations and commented code.

**`requirements.txt`**

Contains the Python libraries required to run the project.

**`.gitignore`**

Specifies files and folders that should not be uploaded to GitHub.

---

## 📊 Dataset

The project uses a small manually created dataset.

| Study Hours | Attendance | Result |
|-------------|------------|--------|
| 1 | 40 | Fail |
| 2 | 50 | Fail |
| 3 | 55 | Fail |
| 4 | 60 | Fail |
| 5 | 70 | Pass |
| 6 | 75 | Pass |
| 7 | 80 | Pass |
| 8 | 90 | Pass |

Target encoding:

```text
0 = Fail
1 = Pass
```

---

## ⚙️ Technologies Used

- Python
- NumPy
- Matplotlib
- Jupyter Notebook

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/neural-network-from-scratch.git
```

Move into the project directory:

```bash
cd neural-network-from-scratch
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
neural_network_from_scratch.ipynb
```

Then run the cells sequentially.

---

## 🧮 Neural Network Calculation

The neuron first calculates the weighted sum:

```text
z = XW + b
```

Where:

- `X` = input features
- `W` = weights
- `b` = bias
- `z` = weighted sum

The weighted sum is passed through the Sigmoid activation function:

```text
sigmoid(z) = 1 / (1 + e^-z)
```

The output is a probability between `0` and `1`.

---

## 🔁 Forward Propagation

During forward propagation:

```text
Input
  ↓
Weighted Sum
  ↓
Activation Function
  ↓
Prediction
```

The model uses:

```python
z = np.dot(X, weights) + bias
prediction = sigmoid(z)
```

---

## 📉 Loss Function

Binary Cross Entropy is used to measure the difference between the actual result and predicted probability.

```text
Low Loss  → Better Prediction
High Loss → Poor Prediction
```

---

## 🔙 Backward Propagation

After calculating the loss, the model calculates gradients to determine how the weights and bias should be changed.

For the sigmoid + binary cross entropy combination:

```python
dz = prediction - y
```

The gradients are then used to update the parameters.

---

## 📈 Gradient Descent

Gradient Descent updates the model parameters using the calculated gradients.

```text
new parameter =
old parameter - learning rate × gradient
```

In the project:

```python
weights = weights - learning_rate * dw
bias = bias - learning_rate * db
```

This process is repeated for multiple epochs so that the model gradually reduces its loss.

---

## 📉 Training Loss

The project stores the loss after every epoch and visualizes it using Matplotlib.

A decreasing loss generally indicates that the model is learning from the training data.

---

## 🎯 Prediction

After training, the model can predict whether a new student is likely to pass.

Example:

```text
Study Hours = 7
Attendance = 85%
```

The model produces a probability and converts it into a binary prediction:

```text
0 → Fail
1 → Pass
```

---

## 🎓 Learning Objective

The main objective of this project is not to build a production-ready model.

It is to understand **how a neural network works internally**.

Instead of directly using TensorFlow or PyTorch, the important mathematical operations are implemented using NumPy.

This helps understand the foundation behind modern deep learning frameworks.

---

## 🔮 Future Improvements

Possible extensions include:

- Add train/test split
- Add more training data
- Add multiple neurons
- Add a hidden layer
- Implement ReLU activation
- Implement multiple activation functions
- Build a multi-layer neural network
- Add confusion matrix
- Calculate precision, recall and F1-score
- Implement the same model using TensorFlow/Keras
- Compare the from-scratch implementation with a deep learning framework

---

## 👨‍💻 Author

**Gaurav Kumar**

GitHub: https://github.com/gaurav-0400