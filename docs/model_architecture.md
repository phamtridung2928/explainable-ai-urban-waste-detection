# Model Architecture

## Overview

The manuscript names the proposed framework **X-EARO-GANet** and describes four main components.

| Component | Role described in the paper | Details to document for reproduction |
|---|---|---|
| Sparse Autoencoder (SAE) | Learns compact feature representations | Layer sizes, latent dimension, sparsity loss, training settings |
| Graph Attention Network (GANet) | Learns relationships among connected urban locations and predicts hotspot levels | Graph construction, node/edge definitions, layers, attention heads |
| Enhanced Artificial Rabbits Optimizer (EARO) | Searches for GANet hyperparameters | Search space, objective, population size, iterations, stopping rule |
| SHAP | Explains feature contributions to predictions | Explainer, background data, target class, summary/local plots |

## Conceptual flow

`Dataset → Preprocessing → SAE → EARO-tuned GANet → Hotspot prediction → SHAP explanations`

This is a conceptual summary of the manuscript, not an executable model graph. The exact graph-building procedure and several implementation details must be documented before the framework can be independently reproduced.
