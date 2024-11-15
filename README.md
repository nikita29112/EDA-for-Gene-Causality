# EDA-for-Gene-Causality
Exploratory Analysis to Find Gene-Phenotype Causality using Embedding Vectors
## Overview
This project investigates potential causal relationships between genes and phenotypes using dimensionality reduction and clustering techniques. It explores whether there are identifiable patterns that separate causal gene-phenotype pairs from non-causal pairs in a high-dimensional embedding space.

## Requirements
To run this project, ensure you have the following libraries installed:

- pandas
- numpy
- sklearn
- umap-learn
- matplotlib
- seaborn
## Files
*opentargets_step2.for_llm.tsv*: Contains phenotype-gene mappings. *opentargets_step2.labels*: Contains true labels for causal relationships. phenotype_embeddings.csv: Contains embeddings for phenotypes. gene_embeddings.csv: Contains embeddings for genes.

## Usage
#### 1. Data Loading and Preprocessing:
Loads the data, cleans up the columns, and hashs the name to generate a unique sampled dataset.

#### 2. Dimensionality Reduction:
Applied PCA, UMAP, and t-SNE to reduce the phenotype and gene embeddings to 2D space. Visualized these reduced vectors with plots.

#### 3. Compute Derived Vectors:
Calculates the Difference Vectors and Cosine Similarity Vectors between gene and phenotype embeddings for further analysis.

#### 4. Cluster Analysis:
Applied K-Means, DBSCAN, and Gaussian Mixture on each reduced vector set (PCA, UMAP, t-SNE) and the derived vectors. Visualized the clusters and analyzed silhouette scores to assess cluster coherence.
