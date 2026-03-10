---
title: Algorithm Unrolling
parent: Inverse Problems
nav_order: 2
---

# Algorithm Unrolling

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Learning to Solve Inverse Problems Using Wasserstein Loss (Adler & Öktem) | [Link](https://arxiv.org/abs/1710.10898) | 2017 | Proposes learned iterative reconstruction using optimal transport loss, connecting deep learning to variational methods. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| fastMRI (Facebook AI / NYU) | [Link](https://fastmri.org/) | Large-scale MRI k-space dataset; standard testbed for evaluating unrolled networks for accelerated MRI reconstruction. |
| LoDoPaB-CT | [Link](https://zenodo.org/record/3384092) | Low-dose CT reconstruction dataset with paired sinogram and image data; widely used for benchmarking unrolled CT methods. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| DeepInverse | [Link](https://github.com/deepinv/deepinv) | PyTorch library with implementations of many unrolled and plug-and-play reconstruction algorithms. |
| fastMRI (Facebook Research) | [Link](https://github.com/facebookresearch/fastMRI) | Contains unrolled network baselines (E2E-VarNet) for accelerated MRI reconstruction. |
