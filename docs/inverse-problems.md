---
title: Inverse Problems
nav_order: 2
has_children: true
---

# Inverse Problems

Inverse problems involve recovering an unknown quantity — an image, signal, or physical parameter — from indirect, incomplete, or noisy observations. They are central to computational imaging: nearly every acquisition system (MRI, CT, radar, astronomy) requires solving an inverse problem. The field draws on signal processing, optimization, statistics, and increasingly deep learning to design principled reconstruction algorithms.

Browse papers by sub-topic using the sidebar, or jump directly to:
[Foundations & Variational Methods](inverse-problems/foundations) · [Algorithm Unrolling](inverse-problems/algorithm-unrolling) · [Plug-and-Play Methods](inverse-problems/plug-and-play) · [Diffusion & Generative Priors](inverse-problems/diffusion-priors)

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| BSD500 (Berkeley Segmentation Dataset) | [Link](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/) | 500 natural images widely used as a benchmark for image restoration and inverse problem methods. |
| DIV2K | [Link](https://data.vision.ee.ethz.ch/cvl/DIV2K/) | 1000 high-resolution images used as a training and evaluation set for image restoration tasks. |
| CBSD68 | [Link](https://github.com/clausmichele/CBSD68-dataset) | Color version of BSD68; standard benchmark for Gaussian denoising and general inverse problem evaluation. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| ODL (Operator Discretization Library) | [Link](https://github.com/odlgroup/odl) | Python library for numerical functional analysis and inverse problems, with support for tomography and iterative solvers. |
| DeepInverse | [Link](https://github.com/deepinv/deepinv) | PyTorch library for solving inverse problems with deep learning, including plug-and-play, unrolling, and diffusion-based methods. |
| SCICO (Scientific Computational Imaging Code) | [Link](https://github.com/lanl/scico) | JAX-based library for scientific inverse problems with support for proximal algorithms and learned priors. |
| BM3D | [Link](https://github.com/gfacciol/bm3d) | Reference implementation of BM3D, a widely used non-local denoising algorithm frequently used as a prior in inverse problem solvers. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
