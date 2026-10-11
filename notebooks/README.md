# Notebook Plan

Suggested notebooks for a transparent research workflow:

1. `01_dataset_audit.ipynb` — inspect schema, missing values, class balance, duplicates, and feature distributions.
2. `02_baseline.ipynb` — create a leakage-safe split and reproduce a simple baseline.
3. `03_sae_representation.ipynb` — train and validate the Sparse Autoencoder.
4. `04_graph_model.ipynb` — document graph construction and train the Graph Attention Network.
5. `05_hyperparameter_search.ipynb` — run the optimizer with a documented search space and compute budget.
6. `06_shap_analysis.ipynb` — generate global and local explanations.
7. `07_route_optimization.ipynb` — only if a concrete routing algorithm and route evaluation are implemented.

Keep notebooks focused and deterministic. Move reusable logic into `src/` as the project matures.
