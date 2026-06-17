# MNIST FNN

A compact, easy-to-read feedforward neural network for classifying handwritten digits from the MNIST dataset. Designed for learning and quick experimentation.

## Highlights
- Minimal PyTorch implementation
- Separate training and evaluation scripts
- Simple to modify for experiments and teaching

## Requirements
- Python 3.8+
- numpy
- torch
- torchvision

Install:

pip install -r requirements.txt

## Usage
- Train:  python train.py --epochs 10 --batch-size 64
- Evaluate:  python evaluate.py --model path\\to\\model.pt

## Files
- model.py — network definition
- train.py — training loop and checkpointing
- evaluate.py — evaluation and metrics
- requirements.txt — dependency list

## License
MIT

