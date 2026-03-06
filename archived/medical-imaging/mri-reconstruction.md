---
title: MRI Reconstruction
parent: Medical Imaging
nav_order: 1
---

# MRI Reconstruction

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Sparse MRI: The Application of Compressed Sensing for Rapid MR Imaging (Lustig et al.) | [Link](https://onlinelibrary.wiley.com/doi/10.1002/mrm.21391) | 2007 | First major paper applying compressed sensing to accelerate MRI acquisition by exploiting image sparsity. |
| Deep Learning for Accelerated MRI — ADMM-Net (Yang et al.) | [Link](https://arxiv.org/abs/1706.07519) | 2017 | Introduces ADMM-Net, an early deep unrolling approach for accelerated MRI reconstruction from undersampled k-space. |
| End-to-End Variational Networks for Accelerated MRI Reconstruction (Sriram et al.) | [Link](https://arxiv.org/abs/2004.06688) | 2020 | Proposes a deep cascade of variational networks for MRI reconstruction; top performer in the fastMRI challenge. |
| Score-Based Diffusion Models for Accelerated MRI (Chung & Ye) | [Link](https://arxiv.org/abs/2110.05243) | 2022 | Applies diffusion model priors to accelerated MRI reconstruction, enabling high-quality recovery at high acceleration factors. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| fastMRI (Facebook AI / NYU) | [Link](https://fastmri.org/) | Large-scale raw MRI k-space dataset for benchmarking accelerated reconstruction; includes brain and knee scans. |
| IXI Dataset | [Link](https://brain-development.org/ixi-dataset/) | MRI brain images from nearly 600 healthy subjects, used for reconstruction, registration, and segmentation research. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| fastMRI (Facebook Research) | [Link](https://github.com/facebookresearch/fastMRI) | PyTorch codebase with baselines for compressed sensing and deep learning MRI reconstruction. |
| SigPy | [Link](https://github.com/mikgroup/sigpy) | Python library for MRI signal processing with support for parallel imaging, compressed sensing, and k-space operations. |
