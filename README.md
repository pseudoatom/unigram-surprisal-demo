# Unigram Surprisal Demo

The project is based on the paper *Revisiting the Estimation of Unigram Surprisal in Computational Psycholinguistics* by Hopton et al. (EMNLP 2026).

## About

The goal of this project is to reproduce selected results from the paper and build interactive demonstrations of the two estimators.

> [!NOTE]
> The original estimation algorithms are reused from the REPLICA framework.

## Notebooks

| Notebook | Description |
|---|---|
| 01: Original Code Validation | Running the original NMC and MMC implementations. |
| 02: Shared-Sample Comparison | Comparing probability estimates using the same generated texts. |
| 03: Variance Reproduction | Reproducing the available variance results from the paper. |
| 04: Interactive Demo | Exploring estimator variance and comparing common corpus units. |
| 05: Language Model Explorer | Interactive text generation and unigram surprisal estimation using DistilGPT2. |

## Installation

Python 3.12 is recommended.

Clone this repository, create a virtual environment and install the dependencies:

```bash
python3.12 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

> [!TIP]
> A CUDA-enabled GPU is recommended for the language model experiments. The notebooks were tested on Linux with an NVIDIA RTX 4060 Laptop GPU.

Open the notebooks in VS Code or JupyterLab.

Run Notebook 03 before Notebook 04, as it downloads the verification data and prepares the replay environment.

The language model is downloaded automatically when first used.

## Code Attribution

> [!IMPORTANT]
> The original NMC, MMC and bootstrap implementations belong to their respective authors and are reused without modification.
> REPLICA commit used:
> `a0edb776b4f7c68919aeb2f4ead8c43d1ea9247b`

## References

- [Original paper](https://aclanthology.org/2026.emnlp-main.2399/)
- [REPLICA repository](https://github.com/replicaverse/replica)
- [Original study code](https://github.com/replicaverse/replica/tree/main/src/replica/studies/hopton2026unigram)
- [Authors' Data Explorer](https://zhopto3.github.io/unigram/)