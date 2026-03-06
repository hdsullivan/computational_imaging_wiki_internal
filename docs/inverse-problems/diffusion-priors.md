---
title: Diffusion & Generative Priors
parent: Inverse Problems
nav_order: 4
---

# Diffusion & Generative Priors

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Score-Based Generative Modeling through Stochastic Differential Equations (Song et al.) | [Link](https://arxiv.org/abs/2011.13456) | 2021 | Foundation for using score-based diffusion models as priors for solving inverse problems. |
| Diffusion Posterior Sampling for General Noisy Inverse Problems (Chung et al.) | [Link](https://arxiv.org/abs/2209.14687) | 2022 | Practical framework for using diffusion model priors to solve a broad class of linear and nonlinear inverse problems. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| FFHQ (Flickr-Faces-HQ) | [Link](https://github.com/NVlabs/ffhq-dataset) | 70,000 high-quality face images; commonly used to evaluate diffusion-based priors for face restoration inverse problems. |
| fastMRI (Facebook AI / NYU) | [Link](https://fastmri.org/) | MRI k-space dataset used to evaluate diffusion-based priors for accelerated MRI reconstruction. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| Diffusers (HuggingFace) | [Link](https://github.com/huggingface/diffusers) | Standard library for diffusion models; used as backbone for many diffusion-prior inverse problem solvers. |
| DPS (Diffusion Posterior Sampling, official) | [Link](https://github.com/DPS2022/diffusion-posterior-sampling) | Official implementation of DPS for solving noisy linear and nonlinear inverse problems with diffusion priors. |
