# Deep Learning Comparison on MNIST

Comparing several models for handwritten-digit classification on the MNIST dataset, starting from a classic baseline, through a **neural network implemented from scratch in NumPy**, up to Keras models. The point is to see how architecture and optimizer choices affect accuracy, and to spot overfitting.

All the work is in [`mnist_model_comparison.ipynb`](mnist_model_comparison.ipynb).

## What's inside

1. **Data exploration**: loading MNIST (`fetch_openml`), class distribution, and visualizing sample digits.
2. **Baseline**: Logistic Regression (scikit-learn), plus visualization of misclassified digits.
3. **Neural network from scratch**: a fully connected network written only with NumPy (forward pass, backpropagation, SGD, one-hot labels, and saving/loading weights).
4. **Keras models**:
   - Single-layer softmax network
   - FNN with 3 hidden layers (256 → 128 → 64, ReLU, SGD)
   - Improved FNN with 3 wider hidden layers (512 → 256 → 128) and the Adam optimizer
5. **Comparison**: train and validation accuracy curves for all Keras models.

## Results

Trained on a 4,500-image subset; evaluated on the remaining images.

| Model | Test / validation accuracy |
| --- | --- |
| Logistic Regression (scikit-learn) | 88.8% |
| NumPy network from scratch (6 epochs) | 71.3% |
| Keras softmax, 1 layer (20 epochs, Adam) | 90.3% |
| Keras FNN, 3 hidden layers (20 epochs, SGD) | 91.0% |
| Improved FNN, Adam (40 epochs) | **95.2%** |

**Takeaway:** The improved FNN gets the best validation accuracy, but its training accuracy reaches 100% while validation loss stops improving. That is a clear sign of **overfitting**. Natural next steps are dropout, early stopping, training on the full dataset, or a CNN.

## Tech Stack

Python · NumPy · pandas · scikit-learn · TensorFlow / Keras · Matplotlib · Seaborn · Jupyter

## Running

Open the notebook in Jupyter or Google Colab and run the cells in order:

```bash
pip install numpy pandas scikit-learn tensorflow matplotlib seaborn jupyter
jupyter notebook mnist_model_comparison.ipynb
```

> The notebook was originally run on Google Colab. Cells that save models or history to Google Drive can be skipped or pointed to a local path.
