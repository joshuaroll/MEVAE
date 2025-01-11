# MEVAE/MEL - Masked Eigenvalue Learning

## About the Project

The **Masked Eigenvalue Variational Autoencoder (MEVAE)** or **Masked Eigenvalue Learning (MEL)** introduces a novel approach to data masking and reconstruction. By leveraging **Principal Component Analysis (PCA)**, this framework targets the principal components of data, selectively masking subsets for reconstruction. Unlike traditional random masking strategies, which often require dataset-specific hyperparameter tuning, MEVAE/MEL operates stably across datasets without prior assumptions.

Inspired by advances in **Masked Autoencoders** (e.g., scMAE) and structural masking techniques, this approach integrates structured yet data-agnostic masking to enhance generalization and downstream task performance. MEVAE/MEL is particularly suitable for high-dimensional biological datasets like gene expression, offering improved bias reduction and scaling robustness compared to existing methods.

---

## Key Features

- **Masked PCA Learning**: Embeds data into principal components and selectively masks components to reconstruct the original data, bypassing random or structured masking limitations.
- **Stability Across Datasets**: Eliminates the need for optimizing masking ratios, providing robust performance without dataset-specific tuning.
- **Enhanced Generalizability**: Retains global structural information, ensuring better learning and reconstruction of unseen data distributions.
- **Applications in Computational Biology**: Reduces biases due to gene expression scaling and disentangles network-level dependencies, aiding in robust single-cell RNA-seq clustering and other omics analyses.

---

## Motivation

Traditional random masking methods often fail to ensure data generalizability, while structured masking demands prior knowledge of the dataset. MEVAE/MEL's PCA-based masking fills this gap by:

1. Leveraging **global features** inherent in principal components.
2. Enhancing data reconstructions using eigenvector-guided masking.
3. Avoiding the pitfalls of random masking (e.g., redundancy, suboptimal masking ratios) and structured masking (e.g., dataset dependence).

Inspired by the experimental success of **Masked Autoencoders**, MEVAE/MEL extends these concepts to PCA spaces, optimizing latent feature learning and enabling robust predictions.

---

## How It Works

1. **Data Projection**: The input data is transformed into principal components via PCA.
2. **Selective Masking**: Principal components are randomly or systematically masked.
3. **Reconstruction**: The masked components are reconstructed using an encoder-decoder architecture, guided by loss functions emphasizing the reconstruction of global data structures.
4. **General Application**: Supports applications beyond computational biology, offering improved performance in tasks like out-of-distribution learning, dimensionality reduction, and feature disentanglement.

---

## Use Cases

- **Gene Expression Analysis**: Mitigates global biases in high-dimensional datasets, improving clustering and classification in single-cell RNA-seq studies.
- **Biomedical Research**: Identifies rare cell types with higher accuracy by preserving global information while minimizing noise.
- **Out-of-Order Distribution Learning**: Provides a structured approach to data augmentation for robust training pipelines.
