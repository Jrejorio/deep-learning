# Deep Learning Labs

A collection of hands-on deep learning practical works (TPs) in Python, covering the path from a neural network written by hand in NumPy to modern CNN techniques such as Deep Dream, adversarial examples and neural style transfer.

The notebooks are lab exercises from a deep learning course at Télécom Paris. They were created in Google Colab, and each one has an **Open in Colab** badge at the top.

## Contents

| # | Notebook | Topic | Main tools |
|---|----------|-------|-----------|
| 1 | [`MLP_for_classification_from_scratch.ipynb`](MLP_for_classification_from_scratch.ipynb) | Two-layer MLP for binary classification built from scratch: cost function, forward and backward propagation, gradient descent and momentum updates | NumPy, scikit-learn, pandas |
| 2 | [`MLP_for_binary_classification_with_Torch.ipynb`](MLP_for_binary_classification_with_Torch.ipynb) | The same kind of MLP in PyTorch, written three ways: manual tensors with autograd, `nn.Sequential`, and an `nn.Module` subclass | PyTorch, scikit-learn |
| 3 | [`CNN_image_recognition_MNIST.ipynb`](CNN_image_recognition_MNIST.ipynb) | CNN image classification on MNIST and CIFAR-10, plus visualisation of convolutional filters | PyTorch, torchvision |
| 4 | [`CNN_Deep_Dream_and_Adversarial_Examples.ipynb`](CNN_Deep_Dream_and_Adversarial_Examples.ipynb) | Deep Dream (gradient ascent on layer activations) and adversarial examples that fool a pretrained VGG19 | PyTorch, torchvision, PIL |
| 5 | [`Style_transfer_with_CNNs.ipynb`](Style_transfer_with_CNNs.ipynb) | Neural style transfer (Gatys et al.) with content, style (Gram matrix and covariance) and total variation losses, plus colour palette preservation | PyTorch, torchvision, kornia |

The notebooks are meant to be read in this order. Each one builds on ideas from the previous ones.

## Getting started

### Option A: Google Colab (easiest)

Click the **Open in Colab** badge at the top of any notebook on GitHub. No local setup is needed, and you can switch to a free GPU from *Runtime → Change runtime type*. This is recommended for notebooks 3 to 5.

### Option B: Run locally

```bash
# 1. Clone the repository
git clone https://github.com/Jrejorio/deep-learning.git
cd deep-learning

# 2. Create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# 3. Install the dependencies
pip install numpy pandas matplotlib scikit-learn pillow tqdm \
            torch torchvision kornia jupyterlab

# 4. Launch Jupyter
jupyter lab
```

A GPU is not required, but the style transfer and Deep Dream notebooks run much faster with one.

## Notes

- Some cells are lab exercises with blocks marked `# --- START CODE HERE` / `# --- END CODE HERE`. These are the parts to fill in.
- The MNIST and CIFAR-10 datasets, and the pretrained VGG weights, are downloaded automatically on first run. An internet connection is needed.
- `CNN_Deep_Dream_and_Adversarial_Examples.ipynb` (about 29 MB) and `Style_transfer_with_CNNs.ipynb` (about 3.5 MB) are large because they store their output images.

## Credits

The lab material was originally created by the course instructors at Télécom Paris:

- **Geoffroy Peeters**: MLP labs (notebooks 1 and 2)
- **Alasdair Newson** and **Loïc Le Folgoc**: CNN labs (notebooks 3 to 5)

This repository contains my own work and solutions on top of that material.
