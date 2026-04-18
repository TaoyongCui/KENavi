# KENavi

This repository provides visualization results for **KENavi**, a knowledge-enhanced framework for identifying driver genes during cellular state transitions in single-cell data.

KENavi integrates biological knowledge with expression-derived manifold representations to enable robust and interpretable driver gene identification, especially under limited perturbation coverage.

---

## 📌 Project Overview

Identifying **driver genes** that govern transitions between cellular states is a fundamental problem in single-cell biology. However, existing approaches often rely purely on expression data, which becomes unreliable under:

- Sparse perturbation coverage  
- Cross-condition generalization  
- Noisy or heterogeneous cellular responses  

**KENavi addresses this limitation by incorporating external biological knowledge into the representation learning process**, improving both stability and interpretability.

---



## 📊 UMAP Visualization

**File: `UMAP.png`**

This figure visualizes the learned cell embeddings under three different scenarios:

- **Training T cell dataset**
- **Validation T cell dataset**
- **Real-world T cell differentiation dataset (test set)**

### Key observations:

- The learned manifold preserves clear biological structure across datasets  
- Validation data aligns well with training distribution  
- Test data (real differentiation scenario) remains well-structured, indicating strong generalization  

This demonstrates that KENavi learns **stable and transferable representations** of cellular states.

---

## 🧪 Driver Gene Prediction Results

The following figures illustrate the predicted importance (ranking) of key genes across T cell differentiation stages:

### 1. `GATA-3.png`
- GATA3 is a well-known regulator in T cell differentiation  
- KENavi captures its dynamic importance across stages  

### 2. `CD27.png`
- CD27 is associated with T cell activation and memory formation  
- The model identifies stage-specific relevance  

### 3. `IL2.png`
- IL2 plays a critical role in T cell proliferation and signaling  
- KENavi successfully reflects its functional role during transitions  

### Interpretation:

Across all genes, KENavi consistently captures:

- **Stage-specific regulatory importance**
- **Dynamic changes along differentiation trajectories**
- **Biologically meaningful ranking patterns**

---

## 🔍 Key Insights

- KENavi improves **driver gene identification** beyond expression-only methods  
- Knowledge integration leads to:
  - Better generalization  
  - More stable manifold structure  
  - Improved interpretability  

- The model captures **dynamic regulatory programs**, not just static gene importance  


---

## 🚀 Conclusion

KENavi provides a **knowledge-guided framework** for understanding cellular transitions and identifying key regulatory genes.  
The results demonstrate that incorporating biological knowledge is essential for robust and generalizable inference in single-cell systems.

---

## 📬 Contact

For questions or collaborations, please contact the repository owner.
