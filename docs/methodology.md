# Methodology

This document summarizes the methods described in the research manuscript. It does not claim that the experiments have been independently reproduced.

## 1. Data preparation

The paper describes the following preprocessing steps:

- Missing-value imputation
- Interquartile range (IQR) filtering for outliers
- Min–Max normalization

For a reproducible implementation, fit imputation and scaling parameters on the training split only, then apply those fitted transformations to validation and test data. Document whether outlier filtering is performed before or after the split.

## 2. Sparse Autoencoder (SAE)

The paper uses a Sparse Autoencoder to learn compact latent representations from the input features and reduce redundancy.

Implementation details still needed include the encoder/decoder architecture, latent dimension, sparsity penalty, optimizer, stopping criteria, and random seed.

## 3. Graph Attention Network (GANet)

The paper describes a Graph Attention Network that models spatial relationships among urban locations by weighting neighboring nodes.

A reproducible implementation must specify:
- What each graph node represents
- How edges are created (for example, from geographic proximity or road-network connectivity)
- Which node and edge features are used
- Number of layers, attention heads, hidden dimensions, and regularization
- How predictions map to `waste_hotspot_level`

## 4. Enhanced Artificial Rabbits Optimizer (EARO)

The paper describes EARO as an improved metaheuristic used to optimize GANet hyperparameters.

The repository should eventually specify the search space, population size, stopping condition, objective metric, compute budget, and implementation source for EARO.

## 5. SHAP explainability

The paper uses SHAP to explain predictions and reports bin fill level, waste weight, and overflow count/frequency among the most important features.

A reproduction should include the SHAP explainer type, background sample, evaluated sample, class being explained, and both global and local explanations.

## 6. Route optimization scope

Although route optimization appears in the paper title and stated objective, the described results primarily report hotspot-classification metrics. A complete route-optimization implementation should define the routing problem, constraints, objective function, route algorithm, and route-specific evaluation metrics (for example, distance or time versus a baseline).
