# KENavi

This repository provides visualization results for **KENavi**, Knowledge-Enhanced Navigator of Cell State Transitions.

## Overview

We present both manifold-level visualization and driver gene prediction results across different T cell differentiation stages.

## UMAP Visualization

**UMAP.png**

This figure shows the low-dimensional embedding of single-cell data under three different settings:

- Training T cell data  
- Validation T cell data  
- Real-world T cell differentiation scenario (test data)  

The visualization demonstrates that the learned representation captures consistent and biologically meaningful structure across datasets, and generalizes well to realistic differentiation processes.

## Driver Gene Prediction

The following figures present KENavi-predicted driver gene rankings across different stages of T cell differentiation:

- GATA-3.png  
- CD27.png  
- IL2.png  

Each figure shows how the importance (ranking) of a specific gene evolves during the differentiation trajectory. These genes are known to be associated with T cell development and functional specialization, and KENavi successfully captures their dynamic regulatory roles.

## Key Insight

- KENavi integrates biological knowledge with expression-based manifold learning  
- Enables robust driver gene identification under limited perturbation coverage  
- Captures stage-specific gene regulation dynamics in T cell differentiation
