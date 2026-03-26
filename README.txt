# Denoising Autoencoder Tutorial  
## Learning Robust Representations with Fashion-MNIST

This project demonstrates how **denoising autoencoders (DAEs)** learn robust and meaningful representations by reconstructing clean data from corrupted inputs.

The tutorial focuses on how **noise level** and **bottleneck size** influence:
- reconstruction quality
- feature learning
- downstream classification performance

---

## Project Overview

Autoencoders are neural networks that compress and reconstruct data. However, standard autoencoders may simply memorise inputs without learning useful features.

To address this, **denoising autoencoders** are trained on corrupted inputs while learning to reconstruct the original data. This encourages the model to capture underlying structure rather than noise.

This project provides:
- a conceptual explanation of denoising autoencoders
- a reproducible experimental setup
- visual and quantitative analysis
- evaluation of learned representations

---

## Objectives

The tutorial investigates:

1. **How noise level affects learning**
   - Low noise (10%)
   - Moderate noise (30%)
   - High noise (50%)

2. **How bottleneck size affects representation**
   - 16 units (high compression)
   - 32 units (moderate compression)
   - 64 units (low compression)

3. **Whether learned features are useful**
   - Compared using downstream classification performance

---

## Experimental Setup

### Dataset
- **Fashion-MNIST**
- 70,000 grayscale images (28×28 pixels)
- 10 clothing categories

### Models Implemented
- Standard Autoencoder (baseline)
- Denoising Autoencoder (DAE)
- PCA (linear baseline for comparison)

### Evaluation Metrics
- Reconstruction loss
- Visual reconstruction quality
- Latent space structure (PCA visualisation)
- Classification accuracy (logistic regression on latent features)

---

## Key Findings

- Moderate noise (~30%) produced the best balance between robustness and reconstruction quality  
- Very high noise (50%) degraded performance due to excessive information loss  
- Smaller bottlenecks enforced compression but reduced detail  
- Denoising autoencoders learned **more meaningful representations** than standard autoencoders  
- Latent features from DAE improved classification accuracy compared to raw pixels and PCA  

---

##  Why This Matters

Denoising autoencoders are not just reconstruction models — they are powerful tools for:

- feature extraction  
- dimensionality reduction  
- noise-robust learning  
- preprocessing for downstream tasks  

This makes them useful in real-world applications such as:
- image denoising  
- anomaly detection  
- medical imaging  
- representation learning  

---

## Repository Structure

```text
denoising-autoencoder-tutorial/
│
├── notebooks/
│ └── denoising_autoencoder_fashion_mnist.ipynb
│
├── tutorial/
│ └── denoising_autoencoder_tutorial.pdf
│
├── figures/
│ ├── reconstructions.png
│ ├── loss_curves.png
│ ├── latent_space.png
│
├── requirements.txt
├── README.md
└── LICENSE
```
---

##  Installation & Usage

### 1. Clone the repository
```bash
git clone https://github.com/your-username/denoising-autoencoder-tutorial.git
cd denoising-autoencoder-tutorial
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook notebooks/denoising_autoencoder_fashion_mnist.ipynb
```

Run all cells to reproduce results and figures.

---

## Accessibility

This project was designed with accessibility in mind:

 - high-contrast and readable plots
 - descriptive captions for all figures
 - clear structure and simple explanations
 - avoids colour-only distinctions (colour-blind friendly)
 - notebook includes comments explaining each step

---
 ## Ethical Considerations

Although Fashion-MNIST does not contain personal data, real-world datasets may introduce bias.

Important considerations include:

 - ensuring diverse and representative datasets
 - avoiding loss of critical features during denoising
 - transparency in model limitations
---

## References
Goodfellow, I. et al. (2016). Deep Learning
Vincent, P. et al. (2010). Stacked Denoising Autoencoders. JMLR
Xiao, H. et al. (2017). Fashion-MNIST Dataset. arXiv

---
## License

This project is licensed under the MIT License.
You are free to use, modify, and distribute this work with proper attribution.

## Author
Ebenezer Okunola


