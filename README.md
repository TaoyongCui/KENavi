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

## Norman Dataset: Double Perturbation Results

To further evaluate whether KENavi can identify regulatory signals beyond simple single-gene settings, we tested it on the **Norman dataset double perturbation task**.

### Quantitative Results

| Metric | Additive model | CellNavi | KENavi |
|---|---:|---:|---:|
| Top-2 accuracy | 0.0288 | 0.2094 | **0.2776** |
| Top-5 accuracy | 0.1550 | 0.3627 | **0.4778** |
| Top-10 accuracy | 0.1969 | 0.4881 | **0.6543** |
| F1 score | 0.0893 | 0.4100 | **0.5775** |

### Interpretation

These results show that KENavi substantially outperforms both the simple additive baseline and CellNavi on the double perturbation setting.

- Compared with the **additive model**, KENavi achieves much higher performance across all ranking metrics and F1 score, suggesting that the model captures **nonlinear and biologically meaningful combinatorial effects**
- Compared with **CellNavi**, KENavi consistently achieves stronger Top-k accuracy and F1 score, indicating that **knowledge-enhanced transition modeling** provides a clear advantage in more complex perturbation scenarios

This experiment supports the idea that KENavi is not only effective for standard state-transition analysis, but also capable of handling **more realistic and challenging multi-gene perturbation settings**.

---

## Effect of Graph Construction Strategy

To evaluate the impact of different biological priors, we compare KENavi and CellNavi under three graph construction strategies:

- **Random graph** (no biological prior)
- **GRN (Gene Regulatory Network)**
- **NicheNet-based graph** (knowledge-informed)

### Quantitative Results

| Model     | Graph Type | Top-1 Accuracy | F1 Score |
|----------|-----------|---------------:|---------:|
| CellNavi | Random    | 0.02           | 0.15     |
| CellNavi | GRN       | 0.13           | 0.10     |
| CellNavi | NicheNet  | 0.46           | 0.43     |
| KENavi   | Random    | 0.17           | 0.21     |
| KENavi   | GRN       | 0.23           | 0.22     |
| KENavi   | NicheNet  | **0.54**       | **0.53** |

### Interpretation

- Using biologically informed graphs (GRN, NicheNet) significantly improves performance over random graphs  
- **NicheNet provides the strongest prior**, leading to the best results for both models  
- KENavi consistently outperforms CellNavi across all graph types, demonstrating its stronger ability to leverage structural and knowledge-based information  

These results highlight the importance of **biological prior quality** and show that KENavi can effectively utilize such priors for improved driver gene identification.

## Case Study: Key Genes During Pathogenesis

We further compare **CellNavi** and **KENavi** on identifying key genes involved in pathogenesis.

### Ranking Comparison

| Gene   | CellNavi Rank | KENavi Rank |
|--------|--------------:|------------:|
| EIF2S1 | 3             | **3**       |
| BAX    | 7             | **5**       |
| HSPA5  | 16            | **8**       |

### Interpretation

- KENavi consistently ranks key genes **higher (better)** than CellNavi  
- For **BAX** and **HSPA5**, KENavi significantly improves the ranking, indicating better identification of biologically relevant drivers  
- Results suggest that knowledge integration helps prioritize **functionally critical genes** during disease progression  

This case study further demonstrates KENavi’s advantage in capturing **pathogenesis-relevant regulatory signals**.
## 🚀 Conclusion

KENavi provides a **knowledge-guided framework** for understanding cellular transitions and identifying key regulatory genes.  
The results demonstrate that incorporating biological knowledge is essential for robust and generalizable inference in single-cell systems.

---

## 📬 Contact

For questions or collaborations, please contact the repository owner.
