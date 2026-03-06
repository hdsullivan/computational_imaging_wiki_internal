---
title: Compressed Sensing
nav_order: 4
---

# Compressed Sensing

Compressed sensing (or compressive sensing) establishes that sparse signals can be recovered exactly — or with high probability — from far fewer measurements than classical Nyquist sampling would require, provided the measurements are incoherent with the signal's sparse representation. It has had a transformative impact on MRI, single-pixel cameras, radar, and many other imaging modalities, and provides the theoretical backbone for much of modern underdetermined inverse problems.

---

## Foundational & Highly Cited Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Compressed Sensing (Donoho) | [Link](https://ieeexplore.ieee.org/document/1614066) | 2006 | Seminal IEEE Transactions paper establishing that sparse signals can be recovered from underdetermined measurements via ℓ₁ minimization. |
| Robust Uncertainty Principles: Exact Signal Recovery from Highly Incomplete Frequency Information (Candès, Romberg, Tao) | [Link](https://arxiv.org/abs/math/0409186) | 2006 | Proves exact recovery of sparse signals from incomplete Fourier measurements, foundational to compressed sensing theory. |
| Near-Optimal Signal Recovery from Random Projections (Candès, Tao) | [Link](https://arxiv.org/abs/math/0410542) | 2006 | Introduces the restricted isometry property (RIP) and proves near-optimal recovery bounds from random measurements. |
| An Introduction to Compressive Sampling (Candès, Wakin) | [Link](https://ieeexplore.ieee.org/document/4472240) | 2008 | Accessible tutorial overview of compressed sensing theory, widely read as an entry point to the field. |
| Sparse MRI: The Application of Compressed Sensing for Rapid MR Imaging (Lustig et al.) | [Link](https://onlinelibrary.wiley.com/doi/10.1002/mrm.21391) | 2007 | First major demonstration of compressed sensing applied to MRI, enabling dramatic acceleration of scan times. |
| Iterative Hard Thresholding for Compressed Sensing (Blumensath, Davies) | [Link](https://arxiv.org/abs/0805.0510) | 2009 | Proposes IHT, a computationally efficient algorithm for sparse recovery with provable convergence guarantees. |

---

## Datasets

| Title | Link | Description |
|-------|------|-------------|
| Sparco: A Testing Framework for Sparse Reconstruction | [Link](https://friedlander.io/sparco/) | Collection of test problems for sparse recovery algorithms, commonly used to benchmark compressed sensing methods. |
| fastMRI Dataset (Facebook/NYU) | [Link](https://fastmri.org/) | Large-scale MRI dataset designed for benchmarking compressed sensing and deep learning-based MRI reconstruction. |
| Single-Pixel Camera Datasets (Rice DSP Group) | [Link](https://dsp.rice.edu/cs/) | Benchmark data and resources from the Rice group that pioneered the single-pixel compressed sensing camera. |

---

## Code & Software

| Title | Link | Description |
|-------|------|-------------|
| SPGL1 | [Link](https://github.com/mpf/spgl1) | Widely used solver for sparse recovery via the LASSO, BPDN, and basis pursuit using spectral projected gradient. |
| CVXPY | [Link](https://github.com/cvxpy/cvxpy) | Python-embedded convex optimization library; standard tool for formulating and solving compressed sensing problems. |
| TFOCS (Templates for First-Order Conic Solvers) | [Link](https://github.com/cvxr/TFOCS) | MATLAB library for first-order methods in compressed sensing and related convex programs. |
| SigPy | [Link](https://github.com/mikgroup/sigpy) | Python library for signal processing and compressed sensing, with strong support for MRI applications. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../CONTRIBUTING.md) before submitting.
