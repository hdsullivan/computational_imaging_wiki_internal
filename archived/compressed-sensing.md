---
title: Compressed Sensing
nav_order: 4
has_children: true
---

# Compressed Sensing

Compressed sensing establishes that sparse signals can be recovered exactly from far fewer measurements than classical Nyquist sampling would require, provided the measurements are incoherent with the signal's sparse representation. It has had a transformative impact on MRI, single-pixel cameras, radar, and many other imaging modalities, and provides the theoretical backbone for much of modern underdetermined inverse problems.

Browse papers by sub-topic using the sidebar, or jump directly to:
[Theoretical Foundations](compressed-sensing/theoretical-foundations) · [Recovery Algorithms](compressed-sensing/recovery-algorithms) · [Applications](compressed-sensing/applications)

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Sparco: A Testing Framework for Sparse Reconstruction | [Link](https://friedlander.io/sparco/) | Collection of test problems for sparse recovery algorithms, commonly used to benchmark compressed sensing methods. |
| fastMRI Dataset (Facebook/NYU) | [Link](https://fastmri.org/) | Large-scale MRI dataset designed for benchmarking compressed sensing and deep learning-based MRI reconstruction. |
| Single-Pixel Camera Datasets (Rice DSP Group) | [Link](https://dsp.rice.edu/cs/) | Benchmark data and resources from the Rice group that pioneered the single-pixel compressed sensing camera. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| SPGL1 | [Link](https://github.com/mpf/spgl1) | Widely used solver for sparse recovery via the LASSO, BPDN, and basis pursuit using spectral projected gradient. |
| CVXPY | [Link](https://github.com/cvxpy/cvxpy) | Python-embedded convex optimization library; standard tool for formulating and solving compressed sensing problems. |
| TFOCS (Templates for First-Order Conic Solvers) | [Link](https://github.com/cvxr/TFOCS) | MATLAB library for first-order methods in compressed sensing and related convex programs. |
| SigPy | [Link](https://github.com/mikgroup/sigpy) | Python library for signal processing and compressed sensing, with strong support for MRI applications. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
