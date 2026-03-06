---
title: Denoising
parent: Image Reconstruction
nav_order: 1
---

# Denoising

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Beyond a Gaussian Denoiser: Residual Learning of Deep CNN for Image Denoising (DnCNN) (Zhang et al.) | [Link](https://arxiv.org/abs/1608.03981) | 2017 | Introduces DnCNN, an influential residual learning architecture for Gaussian denoising that also handles blind denoising and JPEG artifact removal. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| BSD68 / CBSD68 | [Link](https://github.com/clausmichele/CBSD68-dataset) | 68 grayscale/color natural images; the standard benchmark for evaluating Gaussian denoising algorithms. |
| SIDD (Smartphone Image Denoising Dataset) | [Link](https://www.eecs.yorku.ca/~kamel/sidd/) | Real noisy image pairs from smartphones; the primary benchmark for real-noise denoising beyond synthetic Gaussian noise. |
| PolyU Real-World Noisy Images | [Link](https://github.com/csjunxu/PolyU-Real-World-Noisy-Images-Dataset) | Real noisy/clean image pairs captured under controlled conditions for evaluating real-world denoising methods. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| DnCNN (official) | [Link](https://github.com/cszn/DnCNN) | Original MATLAB/PyTorch implementation of DnCNN, FFDNet, and other residual denoising networks. |
| BasicSR | [Link](https://github.com/XPixelGroup/BasicSR) | PyTorch training framework that includes implementations of DnCNN, RealESRGAN, and other restoration models. |
