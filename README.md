# Protein-Sequence-ML
# Unsupervised and Supervised Analysis of Protein Sequences

**Computational Science — Machine Learning for Physicists** (2022/2023)  
by **Davide Rossetti** and **Persia Kamali**.

---

## 🧬 Overview

This project applies core machine learning methods to the analysis of protein sequence data. We investigate how unsupervised and supervised learning techniques can extract structural and functional information from natural and artificially generated protein multiple sequence alignments (MSA).

---

## ⚙️ Methodology

1. **Encoding** – One-hot representation of amino-acid sequences  
2. **Dimensionality Reduction** – Principal Component Analysis (PCA)  
3. **Clustering** – K-Means, DBSCAN, and hierarchical methods  
4. **Classification** – Logistic Regression to predict protein functionality  
5. **Generative Modeling** – Pseudolikelihood maximization with Gibbs sampling  

---

## 📊 Results

### Dimensionality Reduction
- PCA on natural sequences shows **no clear separation** between functional and non-functional proteins in 2D.  
- Artificial sequences project onto nearly the same region, indicating that the generative model reproduces the global statistics of the data.

### Clustering
- Unsupervised algorithms (K-Means, DBSCAN, Agglomerative) **failed to separate functional groups**.  
- Cluster purity ≈ 70%, confirming that simple sequence statistics do not capture functionality.

### Classification
- Logistic Regression trained on natural data achieved:  
  - **81 % accuracy** on validation  
  - **76 % on test** (natural sequences)  
  - **77 % on artificial sequences**  
- Generated sequences are statistically consistent with natural data, but functional distinction remains subtle.

### Generative Model
- Using pseudolikelihood estimation and Gibbs sampling, **540 artificial sequences** were generated.  
- Only **24 %** were predicted functional, showing partial success in reproducing biologically relevant properties.

### Interpretation
Protein functionality is **not linearly separable** in one-hot or PCA space. The generative model captures realistic sequence patterns but not the complex features driving function, highlighting the limitations of purely statistical learning for biological sequence analysis.



