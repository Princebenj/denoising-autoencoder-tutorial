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
│ ├── reconstruction_comparison.png
│ ├── validation_loss_curves.png
│ ├── corruption_examples.png
│ ├── latent_space_pca.png
│ ├── sample_images.png
│ ├── loss_heatmap.png



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
Chollet, F. et al. (2015) Keras. Available at: https://keras.io (Accessed: 27 March 2026)
Goodfellow, I., Bengio, Y. and Courville, A. (2016) Deep Learning. Cambridge, MA: MIT Press. Available at: https://www.deeplearningbook.org (Accessed: 27 March 2026)

Pedregosa, F. et al. (2011) ‘Scikit-learn: Machine learning in Python’, Journal of Machine Learning Research, 12, pp. 2825–2830. Available at: https://scikit-learn.org (Accessed: 27 March 2026)

Vincent, P., Larochelle, H., Bengio, Y. and Manzagol, P.-A. (2008) ‘Extracting and composing robust features with denoising autoencoders’, Proceedings of the 25th International Conference on Machine Learning (ICML), pp. 1096–1103. Available at: https://dl.acm.org/doi/10.1145/1390156.1390294 (Accessed: 27 March 2026)

Wong, B. (2011) ‘Color blindness’, Nature Methods, 8(6), p. 441. Available at: https://doi.org/10.1038/nmeth.1618 (Accessed: 27 March 2026)

Xiao, H., Rasul, K. and Vollgraf, R. (2017) ‘Fashion-MNIST: a novel image dataset for benchmarking machine learning algorithms’, arXiv:1708.07747. Available at: https://arxiv.org/abs/1708.07747 (Accessed: 27 March 2026)

---
## License

This project is licensed under the MIT License.
You are free to use, modify, and distribute this work with proper attribution.

## Author
Ebenezer Okunola

24119439

