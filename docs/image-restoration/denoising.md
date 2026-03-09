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

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing** — work that has moved the field or is poised to. Incremental improvements belong in linked reading lists, not here. [Read the Contribution Guide](../../contributing/) before submitting.

### Classical & Statistical Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| A Non-Local Algorithm for Image Denoising (NLM) (Buades et al.) | [Link](https://ieeexplore.ieee.org/document/1467423) | 2005 | Introduces non-local means: each pixel is restored as a weighted average of all pixels with similar local neighborhoods. Established non-local self-similarity as a foundational prior for image restoration. |
| Image Denoising by Sparse 3D Transform-Domain Collaborative Filtering (BM3D) (Dabov et al.) | [Link](https://ieeexplore.ieee.org/document/4271520) | 2007 | BM3D groups similar 2D patches into 3D stacks, applies collaborative hard-thresholding in the transform domain, and aggregates. Remained the standard AWGN denoising benchmark for over a decade. |
| K-SVD: An Algorithm for Designing Overcomplete Dictionaries for Sparse Representation (Aharon et al.) | [Link](https://ieeexplore.ieee.org/document/1710377) | 2006 | Learns a patch dictionary directly from noisy images; denoising is done by sparse coding each patch over the learned dictionary. Influential in dictionary-learning approaches to image restoration. |
| Weighted Nuclear Norm Minimization with Application to Image Denoising (WNNM) (Gu et al.) | [Link](https://ieeexplore.ieee.org/document/6909921) | 2014 | Groups similar patches and denoises by minimizing a weighted nuclear norm of the stacked patch matrix. Strong non-local prior; competitive with BM3D on AWGN benchmarks. |

### Deep Learning Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Beyond a Gaussian Denoiser: Residual Learning of Deep CNN for Image Denoising (DnCNN) (Zhang et al.) | [Link](https://arxiv.org/abs/1608.03981) | 2017 | Introduces DnCNN: a residual CNN that learns the noise rather than the clean image. Achieves strong blind Gaussian denoising and generalizes to JPEG artifact removal. Highly influential in learned image restoration. |
| FFDNet: Toward a Fast and Flexible Solution for CNN-Based Image Denoising (Zhang et al.) | [Link](https://ieeexplore.ieee.org/document/8365806) | 2018 | Extends DnCNN by accepting a tunable noise level map as input, enabling flexible control over denoising strength and handling spatially varying noise without retraining. |
| Toward Convolutional Blind Denoising of Real Photographs (CBDNet) (Guo et al.) | [Link](https://arxiv.org/abs/1807.04686) | 2019 | A two-stage network that first estimates a spatially varying noise map and then performs denoising conditioned on it. One of the first DL methods to seriously address real camera noise. |
| Real Image Denoising with Feature Attention (RIDNet) (Anwar & Barnes) | [Link](https://arxiv.org/abs/1904.07396) | 2019 | Single-stage network with feature attention modules trained on real noise datasets. Achieves strong performance on SIDD and DND without the explicit noise estimation stage. |
| Plug-and-Play Image Restoration with Deep Denoiser Prior (DRUNet) (Zhang et al.) | [Link](https://arxiv.org/abs/2008.13751) | 2021 | Proposes DRUNet — a powerful UNet-based denoiser — and demonstrates its use as a learned prior in half-quadratic splitting (HQS) for a range of inverse problems. Widely used as a denoiser in plug-and-play solvers. |
| Restormer: Efficient Transformer for High-Resolution Image Restoration (Zamir et al.) | [Link](https://arxiv.org/abs/2111.09881) | 2022 | Transformer-based architecture with multi-DConv head transposed attention (MDTA) and gated-Dconv feed-forward networks. Achieves SOTA on Gaussian denoising, real denoising, and motion deblurring. |
| Simple Baselines for Image Restoration (NAFNet) (Chen et al.) | [Link](https://arxiv.org/abs/2204.04676) | 2022 | Shows that a simple nonlinear activation free network matches or exceeds complex transformer designs. Sets strong baselines on SIDD, GoPro, and REDS with high computational efficiency. |

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
| BM3D (reference implementation) | [Link](https://github.com/gfacciol/bm3d) | Python port of the original BM3D algorithm; widely used as a classical baseline and as a prior in inverse problem solvers. |
| Restormer (official) | [Link](https://github.com/swz30/Restormer) | Official PyTorch implementation with pretrained models for Gaussian denoising, real denoising, and motion deblurring. |
| BasicSR | [Link](https://github.com/XPixelGroup/BasicSR) | General-purpose PyTorch restoration framework with implementations of DnCNN, RealESRGAN, and many other restoration models; well-maintained and widely used for benchmarking. |
| KAIR (Image Restoration Toolbox) | [Link](https://github.com/cszn/KAIR) | Comprehensive toolbox from Kai Zhang including DnCNN, FFDNet, DRUNet, IRCNN, and others; supports plug-and-play integration. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../../contributing/) before submitting.
