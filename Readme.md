# Reproducing and Extending LMCCS

This repository contains the code, experiments, and report for reproducing and extending the paper:

**“Maximum Common Subgraph Guided Graph Retrieval: Late and Early Interaction Networks”**  
by Roy et al. (2022)

The project focuses on reproducing the LMCCS model ablation experiments and performing an additional sensitivity analysis on the noise-filter temperature hyperparameter \(\lambda\).

---

## Project Overview

The main contributions of this work are:

- Reproduction of the LMCCS gossip-network ablation on the MSRC-21 dataset
- Reproduction of the noise-filter ablation
- A 13-point temperature sensitivity sweep for the noise-filter parameter \(\lambda\)
- Analysis of robustness and catastrophic failure regimes

Key findings:

- Removing the gossip network increases test MSE by approximately **2.43×**
- Removing the noise filter causes almost no degradation on MSRC-21
- The model is robust across a wide range of \(\lambda \in [0.1, 10]\)
- Performance collapses at very high temperatures (\(\lambda = 50\))

---

## Dataset and Main Training Code

The original codebase and dataset used for experiments can be accessed here:

https://drive.google.com/drive/u/0/folders/1WLKTK7l3thzqb05qDspLMpic3WvuMHq-


## Experimental Setup

- GPU: NVIDIA P100
- Framework: PyTorch 2.4.0 + CUDA 11.8
- Dataset: `msrc_21_500qgrlarge`
- Evaluation Metrics:
  - Mean Squared Error (MSE)
  - Kendall’s Tau (KTau)

---

## Report

The full project report is included in this repository.

---

## Reference

```bibtex
@article{roy2022mcs,
  title={Maximum Common Subgraph Guided Graph Retrieval:
         Late and Early Interaction Networks},
  author={Roy, I. and Chakrabarti, S. and De, A.},
  journal={arXiv preprint arXiv:2210.11020},
  year={2022}
}
```

---

## Author

Rahul Kumar  
M.Tech Systems and Control Engineering  
IIT Bombay
