---
title: Super-Resolution
parent: Image Reconstruction
nav_order: 3
---

# Super-Resolution

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Image Super-Resolution Using Deep Convolutional Networks (SRCNN) (Dong et al.) | [Link](https://arxiv.org/abs/1501.00092) | 2015 | First work applying a deep CNN to single-image super-resolution; foundational to the explosion of DL-based SR methods. |
| Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network (SRGAN) (Ledig et al.) | [Link](https://arxiv.org/abs/1609.04802) | 2017 | Proposes SRGAN, using perceptual and adversarial losses to produce perceptually sharp super-resolved images. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Set5 / Set14 | [Link](https://github.com/jbhuang0604/SelfExSR) | Small standard image sets that appear in nearly every SR paper; used for PSNR/SSIM benchmarking across scales. |
| DIV2K | [Link](https://data.vision.ee.ethz.ch/cvl/DIV2K/) | 1000 high-resolution images; the primary training and validation set for modern single-image super-resolution. |
| Urban100 | [Link](https://github.com/jbhuang0604/SelfExSR) | 100 high-resolution urban scene images emphasizing structures and patterns; benchmark for texture-rich SR evaluation. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| BasicSR | [Link](https://github.com/XPixelGroup/BasicSR) | PyTorch toolkit implementing SRCNN, ESRGAN, Real-ESRGAN, and other canonical SR models with training pipelines. |
| Real-ESRGAN | [Link](https://github.com/xinntao/Real-ESRGAN) | Practical blind super-resolution for real-world degraded images; widely used for upscaling natural images. |
