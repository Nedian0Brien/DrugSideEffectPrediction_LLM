<div align="center">

# DrugSideEffectPrediction_LLM

**Research notebooks for drug-side-effect prediction with embedding similarity analysis**

![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Embeddings](https://img.shields.io/badge/Embeddings-0EA5E9?style=flat-square) ![Research](https://img.shields.io/badge/Research-111827?style=flat-square)

[한국어](./README.md)

</div>

---

## Overview

This repository contains research notebooks that explore drug-side-effect relationships through embeddings, cosine similarity, and real-case validation.

It is currently a notebook-based experiment archive rather than a packaged library. Reproduction requires checking notebook environments and local data paths first.

The main workflow is to place drug and adverse-effect text in an embedding space, calculate candidate relationships with cosine similarity, and then inspect the results through case-validation notebooks. This repository is best read as a research trail rather than a finished model package.

## Highlights

| Area | Description |
|---|---|
| Model result derivation | `모델 결과 도출.ipynb` computes cosine-similarity-based results. |
| Real-case validation | `실제사례검증.ipynb` explores similarity lookup and validation flows. |
| Embedding visualization | `임베딩벡터시각화.ipynb` compares and visualizes embedding vectors. |
| Research checkpoint | Notebook cells and outputs help revisit data paths, model choices, and similarity criteria. |

## Repository Structure

| Path | Role |
|---|---|
| 모델 결과 도출.ipynb | Cosine similarity result generation |
| 실제사례검증.ipynb | Similarity lookup and case validation |
| 임베딩벡터시각화.ipynb | Embedding vector comparison and visualization |

## Reading Order

1. Start with `모델 결과 도출.ipynb` to understand how embedding-based results were produced.
2. Continue with `실제사례검증.ipynb` to see how similarity results were checked against real cases.
3. Use `임베딩벡터시각화.ipynb` to inspect vector distance and distribution visually.

Before running the notebooks, check source data paths and library versions. If a notebook contains an older local path, update the input path before executing cells.

## Quick Start

### Start Jupyter

```bash
jupyter lab
```

### List notebooks

```bash
find . -maxdepth 2 -name "*.ipynb"
```

### Suggested order

모델 결과 도출.ipynb -> 실제사례검증.ipynb -> 임베딩벡터시각화.ipynb

## Verification

| Check | Command |
|---|---|
| Notebook presence | `find . -name "*.ipynb" | wc -l` |

## Operational Notes

- Some notebooks may contain local paths or external data assumptions; inspect paths before running.
- For reproducible research, document input data, model choices, and embedding generation steps separately.
- Follow-up experiments should record data provenance, preprocessing rules, embedding model names, and cosine similarity thresholds.

## Documentation Sources

This README was written from the following files and documents in this repository.

- `모델 결과 도출.ipynb`
- `실제사례검증.ipynb`
- `임베딩벡터시각화.ipynb`
