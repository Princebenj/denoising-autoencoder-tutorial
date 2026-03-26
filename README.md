# Learning Robust Representations with Denoising Autoencoders - ML Tutorial
Author: Ebenezer Okunola
Student ID : 24119439
Course: Machine Learning

# OVERVIEW
This repository contains a tutorial and notebook for a machine-learning assignment focused on **denoising autoencoders** and how **noise level** and **bottleneck size** affect reconstruction quality and learned representations on **Fashion-MNIST**.

## Repository contents

- `denoising_autoencoder_tutorial.pdf` - PDF version of the tutorial
- `denoising_autoencoder_fashion_mnist.ipynb` - full notebook used to generate the figures and results
- `requirements.txt` - Python dependencies
- `LICENSE` - MIT licence

## How to run
1. Create a Python environment.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook notebooks/denoising_autoencoder_fashion_mnist.ipynb
```

4. Run all cells from top to bottom.

The notebook downloads Fashion-MNIST using `tensorflow.keras.datasets.fashion_mnist.load_data()`, trains the baseline autoencoder and the denoising-autoencoder variants.

## Reproducibility notes
- Random seeds are fixed where possible.
- Early stopping is used to make training stable.
- The notebook is designed so the examiner can run it and reproduce the tutorial outputs.

## Accessibility notes
- Use descriptive captions for every figure in the tutorial.
- Avoid relying on colour alone when discussing plots.
- Prefer high-contrast figure labels and readable font sizes.


