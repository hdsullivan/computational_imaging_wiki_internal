---
title: Inverse Problems
nav_order: 2
---

# Inverse Problems

Inverse problems involve recovering an unknown quantity — an image, signal, or physical parameter — from indirect, incomplete, or noisy observations. They are central to computational imaging: nearly every acquisition system (MRI, CT, radar, astronomy) requires solving an inverse problem. The field draws on signal processing, optimization, statistics, and increasingly deep learning to design principled reconstruction algorithms.

---

## 📄 Papers


{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing** — work the community broadly recognizes as essential reading. See the [Contribution Guide](../contributing/) for the full criteria.

| Title | Link | Year | Description |
|-------|------|------|-------------|
| A Mathematical Introduction to Compressive Sensing (Foucart & Rauhut) | [Link](https://link.springer.com/book/10.1007/978-0-8176-4948-7) | 2013 | Comprehensive textbook covering the mathematical foundations of sparse recovery and inverse problems. |
| Plug-and-Play ADMM for Image Restoration (Chan et al.) | [Link](https://arxiv.org/abs/1605.01710) | 2016 | Introduces the Plug-and-Play framework, decoupling the prior (denoiser) from the data fidelity term in iterative reconstruction. |
| Learning to Solve Inverse Problems Using Wasserstein Loss (Adler & Öktem) | [Link](https://arxiv.org/abs/1710.10898) | 2017 | Proposes learned iterative reconstruction using optimal transport loss, connecting deep learning to variational methods. |
| Solving Inverse Problems with Deep Neural Networks (Ongie et al.) | [Link](https://arxiv.org/abs/2005.06001) | 2020 | Survey of deep learning approaches for inverse problems, covering unrolling, plug-and-play, and generative model priors. |
| Score-Based Generative Modeling through Stochastic Differential Equations (Song et al.) | [Link](https://arxiv.org/abs/2011.13456) | 2021 | Foundation for using score-based diffusion models as priors for solving inverse problems. |
| Diffusion Posterior Sampling for General Noisy Inverse Problems (Chung et al.) | [Link](https://arxiv.org/abs/2209.14687) | 2022 | Practical framework for using diffusion model priors to solve a broad class of linear and nonlinear inverse problems. |

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
