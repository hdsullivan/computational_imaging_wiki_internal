---
title: Theoretical Foundations
parent: Compressed Sensing
nav_order: 1
---

# Theoretical Foundations

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Compressed Sensing (Donoho) | [Link](https://ieeexplore.ieee.org/document/1614066) | 2006 | Seminal IEEE Transactions paper establishing that sparse signals can be recovered from underdetermined measurements via ℓ₁ minimization. |
| Robust Uncertainty Principles: Exact Signal Recovery from Highly Incomplete Frequency Information (Candès, Romberg, Tao) | [Link](https://arxiv.org/abs/math/0409186) | 2006 | Proves exact recovery of sparse signals from incomplete Fourier measurements, foundational to compressed sensing theory. |
| Near-Optimal Signal Recovery from Random Projections (Candès, Tao) | [Link](https://arxiv.org/abs/math/0410542) | 2006 | Introduces the restricted isometry property (RIP) and proves near-optimal recovery bounds from random measurements. |
| An Introduction to Compressive Sampling (Candès, Wakin) | [Link](https://ieeexplore.ieee.org/document/4472240) | 2008 | Accessible tutorial overview of compressed sensing theory, widely read as an entry point to the field. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Sparco: A Testing Framework for Sparse Reconstruction | [Link](https://friedlander.io/sparco/) | Collection of structured test problems for benchmarking sparse recovery algorithms; standard for theoretical comparisons. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| CVXPY | [Link](https://github.com/cvxpy/cvxpy) | Python convex optimization library; standard tool for implementing and solving ℓ₁ minimization and basis pursuit programs. |
| SPGL1 | [Link](https://github.com/mpf/spgl1) | Efficient solver for LASSO and basis pursuit via spectral projected gradient; widely used in theoretical benchmarking. |
