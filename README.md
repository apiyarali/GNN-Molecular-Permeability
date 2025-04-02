# Predicting Blood-Brain Barrier Permeability with Graph Neural Networks

## Overview
This project aims to determine whether certain molecules—caffeine, sucrose, D-glucose, fructose, and acetaminophen (Tylenol)—can pass the blood-brain barrier. To achieve this, we implement a _Message Passing Neural Network_ (MPNN), a type of Graph Neural Network (GNN), to predict the molecular property known as _blood-brain barrier permeability_ (BBBP).

## Motivation
Molecules are naturally represented as undirected graphs, where atoms serve as nodes and chemical bonds as edges. GNNs, such as MPNNs, are increasingly proving useful for molecular property prediction.

Traditional machine learning methods—such as random forests and support vector machines—typically rely on precomputed molecular features (e.g., molecular weight, polarity, charge, and atom counts). In contrast, GNNs work directly on molecular graphs, allowing them to learn meaningful molecular representations from raw structural data, potentially improving prediction accuracy.

## Implementation
- **Graph Representation:** Molecules are modeled as graphs `G = (V, E)`, where `V` represents atoms (nodes) and `E` represents chemical bonds (edges).
- **MPNN Architecture:** We implement a message-passing neural network that:
  1. Aggregates information from neighboring atoms (message passing phase).
  2. Uses this information to predict whether a molecule can cross the blood-brain barrier.
- **Dataset:** A curated dataset of known BBB permeability values for different molecules.
- **Frameworks Used:**
  - TensorFlow/Keras or PyTorch for deep learning.
  - RDKit for molecular data handling.
  - DeepChem for molecular graph processing.

## How to Run
1. Clone this repository:
2. Run the Jupyter Notebook

## Results
- The MPNN successfully learns to predict blood-brain barrier permeability from molecular structures.
- Comparison with traditional models demonstrates the advantages of GNNs in molecular property prediction.
- Key visualizations include molecular graphs and training performance plots.

## References
For more on Graph Neural Networks and Message Passing Neural Networks:
- [A Comprehensive Survey on Graph Neural Networks](https://arxiv.org/abs/1901.00596)
- [Graph Neural Networks: A Review of Methods and Applications](https://arxiv.org/abs/1812.08434)
- [Neural Message Passing for Quantum Chemistry](https://arxiv.org/abs/1704.01212)
- [DeepChem's MPNNModel](https://deepchem.readthedocs.io/en/latest/api_reference/models.html#mpnnmodel)
- [akensert GitHub Repository](http://github.com/akensert)

## Future Work
- Experiment with different GNN architectures.
- Extend the dataset with additional molecules.
- Optimize hyperparameters to improve model accuracy.
