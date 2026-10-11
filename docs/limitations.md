# Limitations and Next Steps

These are methodological questions to resolve when turning the manuscript into a reproducible software project.

## 1. Reproducibility

The paper reports a dataset size and model metrics, but a public implementation should provide code, configuration files, random seeds, and exact dependency versions to make the results reproducible.

## 2. Dataset provenance and generalization

The manuscript identifies a Kaggle dataset. Its feature definitions, labels, geographic coverage, collection process, and suitability for claims about real-world urban environments should be checked. The paper itself notes that dataset diversity may limit applicability to other cities.

## 3. Data leakage risks

Preprocessing operations such as imputation, normalization, feature selection, and outlier filtering should be fitted or decided using training data only where applicable. Confirm that test data did not influence preprocessing or hyperparameter selection.

## 4. Graph construction

A Graph Attention Network requires a graph definition. The repository should explain how locations become nodes and how edges are created. Without this, the spatial-learning component is difficult to reproduce.

## 5. Baseline breadth and ablation

The manuscript compares against DT+BPSO. Additional appropriate baselines and ablation experiments would help clarify whether the improvement comes from the architecture, feature representation, hyperparameter optimizer, or other experimental choices.

## 6. Route optimization evidence

The paper title refers to collection route optimization, but the reported comparison table contains classification metrics. To support a route-optimization claim, implement and evaluate a routing method and report relevant route outcomes.

## 7. SHAP interpretation

Feature importance describes model behavior on the analyzed dataset; it does not establish that a feature causes waste accumulation. State this distinction in any project description.
