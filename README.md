# Deep Learning Comparison on MNIST

A PyTorch implementation comparing feedforward neural network architectures for handwritten digit classification on the MNIST dataset.

---

## Overview

The project demonstrates the implementation, training, and evaluation of neural network models while keeping the code simple and easy to understand.

---

## Features

- PyTorch implementation
- Training pipeline
- Evaluation script
- Model checkpointing
- Easy experimentation

---

## Tech Stack

- Python
- PyTorch
- TorchVision
- NumPy

---

## Project Structure

```
model.py

train.py

evaluate.py

requirements.txt
```

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Usage

Train

```bash
python train.py --epochs 10 --batch-size 64
```

Evaluate

```bash
python evaluate.py --model model.pt
```

---

## Future Improvements

- CNN comparison
- Hyperparameter tuning
- TensorBoard support

---

## License

MIT
