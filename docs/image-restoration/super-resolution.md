---
title: Super-Resolution
parent: Image Restoration
nav_order: 3
---

# Super-Resolution

Single-image super-resolution (SISR) is the task of recovering a high-resolution image $x$ from a low-resolution observation $y$. The classical degradation model is:

$$y = (x \otimes k) \downarrow_s + n$$

where $k$ is a blur kernel, $\downarrow_s$ is a downsampling operator with scale factor $s$, and $n$ is additive noise. SISR is severely ill-posed since many high-resolution images are consistent with a single low-resolution input, so strong image priors are essential.

## Degradation Models

The choice of degradation model has major implications for which methods work in practice:

- **Bicubic downsampling:** The dominant assumption in early deep learning SISR. Assumes a fixed, known downsampling kernel and no noise. Methods trained under this assumption often fail on real photographs, where the actual degradation is unknown.
- **Blur + subsampling:** The kernel $k$ is known (e.g., a Gaussian with a given width) but not necessarily bicubic. The image is first blurred, then uniformly downsampled. This is the classical formulation used in many signal-processing and early deep learning methods (e.g., SRMD, IKC), and is more physically grounded than bicubic-only assumptions. Methods under this model are often evaluated across multiple kernel types and sizes.
- **Blind / real-world SISR:** The degradation kernel $k$ is unknown and spatially varying. Real images suffer from sensor noise, optical aberrations, compression artifacts, and complex ISP processing. Real-ESRGAN and related methods use complex synthetic degradation pipelines during training to bridge the sim-to-real gap.
- **Multi-image SR:** Multiple observations of the same scene (with sub-pixel offsets) are fused to reconstruct a single high-resolution image. Common in satellite imaging and video SR.

## Fidelity vs. Perceptual Quality

A key tension in super-resolution is the distortion-perception tradeoff. PSNR/SSIM-optimizing methods (e.g., SRCNN, EDSR) produce smooth, artifact-free outputs that score well numerically but look over-smoothed. Perceptual / adversarial methods (e.g., SRGAN, ESRGAN) sacrifice PSNR to produce sharper textures that look more realistic to human observers. Neither is universally better; the right choice depends on downstream use.

---

## 📄 Papers
### Classical Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Image Super-Resolution via Sparse Representation (Yang et al.) | [Link](https://ieeexplore.ieee.org/document/5466111) | 2010 | Learns coupled dictionaries for low-resolution and high-resolution patches and reconstructs HR images via sparse coding. A foundational example-based super-resolution method. |
| Anchored Neighborhood Regression for Fast Example-Based Super-Resolution (Timofte et al.) | [Link](https://ieeexplore.ieee.org/document/6751349) | 2013 | Introduces ANR, which approximates local patch regressions using anchors in a learned dictionary, enabling efficient example-based SR. |
| A+: Adjusted Anchored Neighborhood Regression for Fast Super-Resolution (Timofte et al.) | [Link](https://link.springer.com/chapter/10.1007/978-3-319-16817-3_8) | 2014 | Improves ANR by increasing anchor points and refining regressors. Became a widely used classical super-resolution baseline prior to deep learning. |

---

### Deep Learning Methods

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Image Super-Resolution Using Deep Convolutional Networks (SRCNN) (Dong et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/7115171) | 2015 | First CNN-based super-resolution model demonstrating deep learning significantly improves reconstruction quality over classical SR methods. |
| Accurate Image Super-Resolution Using Very Deep Convolutional Networks (VDSR) (Kim et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2016/html/Kim_Accurate_Image_Super-Resolution_CVPR_2016_paper.html) | 2016 | Introduces residual learning and deeper architectures for super-resolution, achieving large PSNR improvements over SRCNN. |
| Enhanced Deep Residual Networks for Single Image Super-Resolution (EDSR) (Lim et al.) | [Link](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w12/html/Lim_Enhanced_Deep_Residual_CVPR_2017_paper.html?ref=https://githubhelp.com) | 2017 | Removes batch normalization from ResNet blocks and increases network capacity, achieving state-of-the-art PSNR performance. |
| Photo-Realistic Single Image Super-Resolution Using GAN (SRGAN) (Ledig et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2017/html/Ledig_Photo-Realistic_Single_Image_CVPR_2017_paper.html) | 2017 | Introduces adversarial training and perceptual loss for generating realistic textures in super-resolved images. |
| ESRGAN: Enhanced Super-Resolution Generative Adversarial Networks (Wang et al.) | [Link](http://openaccess.thecvf.com/content_eccv_2018_workshops/w25/html/Wang_ESRGAN_Enhanced_Super-Resolution_Generative_Adversarial_Networks_ECCVW_2018_paper.html) | 2018 | Improves SRGAN with residual-in-residual dense blocks and relativistic GAN training, producing more realistic perceptual results. |
| Residual Dense Network for Image Super-Resolution (Zhang et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2018/html/Zhang_Residual_Dense_Network_CVPR_2018_paper.html) | 2018 | Introduces residual dense blocks that exploit hierarchical features from all convolutional layers for improved SR performance. |
| Image super-resolution using very deep residual channel attention networks (RCAN) (Zhang et al.) | [Link](https://openaccess.thecvf.com/content_ECCV_2018/html/Yulun_Zhang_Image_Super-Resolution_Using_ECCV_2018_paper.html) | 2018 | Incorporates channel attention mechanisms to better model feature importance in deep super-resolution networks. |
| Zero-Shot Super-Resolution Using Deep Internal Learning (Shocher et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2018/html/Shocher_Zero-Shot_Super-Resolution_Using_CVPR_2018_paper.html) | 2018 | Exploits internal recurrence of information in a single image to train a small image-specific CNN at test time. |
| SwinIR: Image Restoration Using Swin Transformer (Liang et al.) | [Link](https://openaccess.thecvf.com/content/ICCV2021W/AIM/html/Liang_SwinIR_Image_Restoration_Using_Swin_Transformer_ICCVW_2021_paper.html) | 2021 | Applies Swin Transformer architecture to image restoration tasks including super-resolution, achieving state-of-the-art performance on several benchmarks. |
| Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data (Wang et al.) | [Link](http://openaccess.thecvf.com/content/ICCV2021W/AIM/html/Wang_Real-ESRGAN_Training_Real-World_Blind_Super-Resolution_With_Pure_Synthetic_Data_ICCVW_2021_paper.html) | 2021 | Extends ESRGAN to real-world blind super-resolution using a high-order degradation model for training data synthesis. |
| SR3: Image Super-Resolution via Iterative Refinement (Saharia et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/9887996/) | 2021 | Introduces diffusion models for super-resolution by iteratively refining noisy images to produce high-quality HR reconstructions. |
| Exploiting Diffusion Prior for Real-World Image Super-Resolution (StableSR) (Wang et al.) | [Link](https://link.springer.com/article/10.1007/s11263-024-02168-7) | 2023 | Uses pretrained latent diffusion models as generative priors for blind super-resolution with strong perceptual quality. |

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Set5 / Set14 | [Link](https://www.kaggle.com/datasets/ll01dm/set-5-14-super-resolution-dataset) | Small standard image sets used in nearly every SISR paper; the minimum baseline for PSNR/SSIM comparison at ×2, ×3, ×4 upscaling. |
| BSD100 | [Link](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/) | 100 images from the Berkeley Segmentation Dataset; standard benchmark for evaluating texture fidelity in SR. |
| Urban100 | [Link](https://www.kaggle.com/datasets/harshraone/urban100) | 100 high-resolution urban images emphasizing repetitive structures and fine patterns; particularly challenging for SR methods. |
| DIV2K | [Link](https://data.vision.ee.ethz.ch/cvl/DIV2K/) | 1000 high-resolution images with diverse content; the primary training/validation set for modern SISR. Downsampled versions at ×2, ×3, ×4 are the standard training pairs. |
| Flickr2K | [Link](https://github.com/LimBee/NTIRE2017) | 2650 high-resolution images scraped from Flickr; often combined with DIV2K (DF2K) for large-scale SR training. |
| RealSR | [Link](https://github.com/csjcai/RealSR) | Real-world paired LR-HR images captured with a DSLR camera at different focal lengths. Used to evaluate methods under true real-world degradation rather than synthetic downsampling. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| BasicSR | [Link](https://github.com/XPixelGroup/BasicSR) | The standard PyTorch SR training framework; includes SRCNN, EDSR, ESRGAN, Real-ESRGAN, and others with full training pipelines and pretrained models. |
| Real-ESRGAN (official) | [Link](https://github.com/xinntao/Real-ESRGAN) | Official implementation for blind real-world SR; includes pretrained models, inference scripts, and a practical degradation pipeline for training. |
| SwinIR (official) | [Link](https://github.com/JingyunLiang/SwinIR) | Official implementation of SwinIR for SR, denoising, and JPEG artifact removal; pretrained models available for all tasks. |
| EDSR (official) | [Link](https://github.com/sanghyun-son/EDSR-PyTorch) | Official PyTorch implementation of EDSR and MDSR; widely used as a PSNR-oriented SR baseline. |

---

> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../../CONTRIBUTING.md) before submitting.
