---
title: Denoising
parent: Image Restoration
nav_order: 1
---

# Denoising

Image denoising is the task of recovering a clean image $x$ from a corrupted observation $y = x + n$, where $n$ represents noise introduced during image acquisition or transmission. Denoising is one of the most well-studied problems in image processing and serves as a testbed for new priors and regularization strategies that generalize broadly across image restoration.

## Noise Models

The choice of noise model fundamentally shapes both the formulation and the algorithm:

- **Additive White Gaussian Noise (AWGN):** $y = x + n$, $n \sim \mathcal{N}(0, \sigma^2 I)$. The dominant model in the literature; tractable and widely benchmarked. Methods are often evaluated at noise levels $\sigma \in \{15, 25, 50\}$.
- **Poisson noise:** Arises in photon-limited imaging (astronomy, fluorescence microscopy). Noise variance is signal-dependent: $y \sim \text{Poisson}(x)$. Often approximated as Gaussian via a variance-stabilizing transform (VST).
- **Real sensor noise:** In practice, camera noise is a mixture of Poisson shot noise, Gaussian read noise, and fixed-pattern noise, further complicated by the camera ISP pipeline. Real noise is spatially correlated, signal-dependent, and non-stationary — far from the idealized AWGN model.

## Blind vs. Non-Blind Denoising

- **Non-blind denoising:** The noise level $\sigma$ is known at test time and can be used directly by the algorithm (e.g., BM3D, NLM).
- **Blind denoising:** $\sigma$ is unknown and must be estimated or treated as a free variable. DnCNN demonstrated strong blind AWGN denoising by training across a range of noise levels; FFDNet extended this by accepting an explicit noise level map as input, enabling spatially varying noise handling.

## Classical vs. Learned Approaches

Classical methods exploit hand-crafted image priors — non-local self-similarity (NLM, BM3D), sparse coding (K-SVD), or low-rank structure (WNNM) — and remain highly competitive reference points, especially at low noise levels. Deep learning methods learn rich image priors from data and now hold state-of-the-art performance, particularly on real-noise benchmarks where classical assumptions break down.

---
## 📄 Papers

### Classical & Variational Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Nonlinear Total Variation Based Noise Removal Algorithms (Rudin et al.) | [Link](https://www-sciencedirect-com.ornl.idm.oclc.org/science/article/pii/016727899290242F) | 1992 | Introduces total variation (TV) denoising, a variational formulation that preserves edges while removing noise. One of the most influential early image restoration models. |
| Fields of Experts: A Framework for Learning Image Priors (Roth & Black) | [Link](https://ieeexplore.ieee.org/abstract/document/1467533) | 2005 | Introduces learned Markov random field priors using filter responses. A key step toward learning-based statistical models for image restoration. |
| From Learning Models of Natural Image Patches to Whole Image Restoration (Zoran & Weiss) | [Link](https://legacy.sites.fas.harvard.edu/~cs278/papers/zw.pdf) | 2011 | Uses Gaussian mixture models of natural image patches as a prior for image restoration. Demonstrates strong performance across denoising, deblurring, and inpainting. |

---

### Non-Local & Patch-Based Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| A Non-Local Algorithm for Image Denoising (Buades et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/1467423/) | 2005 | Introduces non-local means, where each pixel is restored as a weighted average of pixels with similar neighborhoods. Established non-local self-similarity as a key image prior. |
| K-SVD: An Algorithm for Designing Overcomplete Dictionaries for Sparse Representation (Aharon et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/1710377/) | 2006 | Introduces dictionary learning for sparse patch representations. Denoising is performed via sparse coding over the learned dictionary. |
| Image Denoising by Sparse 3D Transform-Domain Collaborative Filtering (Dabov et al.) | [Link](https://ieeexplore.ieee.org/document/4271520) | 2007 | Introduces BM3D, which groups similar patches into 3D stacks and performs collaborative filtering in the transform domain. Considered the classical state-of-the-art for Gaussian denoising. |
| Weighted Nuclear Norm Minimization with Application to Image Denoising (Gu et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2014/html/Gu_Weighted_Nuclear_Norm_2014_CVPR_paper.html) | 2014 | Uses low-rank modeling of grouped patches for denoising via nuclear norm minimization. A strong non-local method competitive with BM3D. |

---

### Deep Learning Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Beyond a Gaussian Denoiser: Residual Learning of Deep CNN for Image Denoising (Zhang et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/7839189/) | 2017 | Introduces DnCNN, a residual CNN that learns the noise instead of the clean image. A foundational deep denoising architecture and widely used benchmark. |
| FFDNet: Toward a Fast and Flexible Solution for CNN-Based Image Denoising (Zhang et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/8365806/) | 2018 | Extends DnCNN by incorporating a noise-level map input, allowing the network to adapt to varying noise levels without retraining. |
| Toward Convolutional Blind Denoising of Real Photographs (Guo et al.) | [Link](http://openaccess.thecvf.com/content_CVPR_2019/html/Guo_Toward_Convolutional_Blind_Denoising_of_Real_Photographs_CVPR_2019_paper.html) | 2019 | Introduces CBDNet, a two-stage model that estimates a noise map before performing denoising, enabling improved performance on real camera noise. |
| Plug-and-Play Image Restoration with Deep Denoiser Prior (Zhang et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/9454311) | 2021 | Introduces DRUNet, a powerful noise-level conditioned UNet denoiser used for Gaussian and real image denoising and widely adopted in image restoration pipelines. |
| Restormer: Efficient Transformer for High-Resolution Image Restoration (Zamir et al.) | [Link](https://openaccess.thecvf.com/content/CVPR2022/html/Zamir_Restormer_Efficient_Transformer_for_High-Resolution_Image_Restoration_CVPR_2022_paper.html) | 2022 | Transformer-based architecture designed for high-resolution restoration tasks including deblurring. |

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| BSD68 / CBSD68 | [Link](https://github.com/clausmichele/CBSD68-dataset) | 68 grayscale (BSD68) and color (CBSD68) images from the Berkeley Segmentation Dataset; the canonical benchmark for AWGN denoising at noise levels σ = 15, 25, 50. |
| SIDD (Smartphone Image Denoising Dataset) | [Link](https://www.eecs.yorku.ca/~kamel/sidd/) | Real noisy/clean image pairs captured with five smartphone cameras under controlled conditions. The primary benchmark for real-noise denoising; includes a challenge server for blind evaluation. |
| DND (Darmstadt Noise Dataset) (Plötz & Roth) | [Link](https://noise.visinf.tu-darmstadt.de/) | 50 pairs of real noisy images from four consumer cameras with different sensor sizes and ISP settings. A standard real-noise benchmark alongside SIDD; evaluation is submission-based. |
| PolyU Real-World Noisy Images | [Link](https://github.com/csjunxu/PolyU-Real-World-Noisy-Images-Dataset) | 100 real noisy/clean image pairs captured under controlled conditions with multiple exposures to synthesize ground truth. Used to evaluate real-noise methods beyond SIDD and DND. |
| RENOIR | [Link](http://ani.stat.fsu.edu/~abarbu/Renoir.html) | Real noise dataset with pairs captured with two DSLR cameras at different ISO settings. Useful for studying camera-specific noise characteristics. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| DnCNN / FFDNet (official) | [Link](https://github.com/cszn/DnCNN) | Original MATLAB and PyTorch implementations of DnCNN, FFDNet, and related residual denoising networks by Kai Zhang. |
| BM3D | [Link](https://pypi.org/project/bm3d/) | BM3D algorithm; widely used as a classical baseline and as a prior in inverse problem solvers. |
| Restormer (official) | [Link](https://github.com/swz30/Restormer) | Official PyTorch implementation of Restormer; includes pretrained models and evaluation scripts for GoPro and RealBlur. |
| BasicSR | [Link](https://github.com/XPixelGroup/BasicSR) | General-purpose PyTorch restoration framework with implementations of DnCNN, RealESRGAN, and many other restoration models; well-maintained and widely used for benchmarking. |
| KAIR (Image Restoration Toolbox) | [Link](https://github.com/cszn/KAIR) | Comprehensive toolbox from Kai Zhang including DnCNN, FFDNet, DRUNet, IRCNN, and others; supports plug-and-play integration. |

---

> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../../CONTRIBUTING.md) before submitting.
