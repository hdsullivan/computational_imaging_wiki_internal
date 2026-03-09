---
title: Deblurring
parent: Image Restoration
nav_order: 2
---

# Deblurring

Image deblurring (also called image deconvolution) is the task of recovering a sharp image from a blurry observation. The standard image formation model is $y = k ∗ x + \epsilon$, where $y$ is the observed blurry image, $x$ is the unknown sharp image, $k$ is the blur kernel, and $\epsilon$ is noise. Blur arises from camera shake during exposure (motion blur), lens defocus, atmospheric turbulence, or object motion in the scene.

The deblurring problem is fundamentally ill-posed: many sharp images could produce the same blurry observation, making regularization or learned priors essential for recovery. The field distinguishes between **non-blind deblurring** (kernel known) and **blind deblurring** (kernel unknown and must be estimated jointly), with the latter being significantly harder. Modern deep learning methods often bypass explicit kernel estimation entirely, treating deblurring as a direct image-to-image regression problem.

---

# 📄 Papers

## Foundational Image Deconvolution

| Title | Link | Year | Description |
|------|------|------|-------------|
| Bayesian-Based Iterative Method of Image Restoration (Richardson) | [Link](https://opg.optica.org/josa/abstract.cfm?uri=josa-62-1-55) | 1972 | Introduces an iterative maximum-likelihood approach for image restoration under Poisson noise. |
| An Iterative Technique for the Rectification of Observed Distributions (Lucy) | [Link](https://ui.adsabs.harvard.edu/abs/1974AJ.....79..745L/abstract) | 1974 | Independently derives the Richardson–Lucy algorithm, now one of the most widely used deconvolution methods in astronomy and microscopy. |
| Iterative Blind Deconvolution Method (Ayres & Dainty) | [Link](https://opg.optica.org/ol/fulltext.cfm?uri=ol-13-7-547) | 1988 | Early iterative blind deconvolution approach alternating between image and kernel estimation. |

---

## Blind Deblurring & Natural Image Priors

| Title | Link | Year | Description |
|------|------|------|-------------|
| Removing Camera Shake from a Single Photograph (Fergus et al.) | [Link](https://dl.acm.org/doi/abs/10.1145/1179352.1141956) | 2006 | Landmark blind deblurring paper introducing natural image gradient statistics as a prior for kernel estimation. |
| High-Quality Motion Deblurring from a Single Image (Shan et al.) | [Link](https://dl.acm.org/doi/10.1145/1399504.1360672) | 2008 | Introduces improved probabilistic modeling of ringing artifacts and noise in blind deblurring. |
| Understanding Blind Deconvolution Algorithms (Levin et al.) | [Link](https://ieeexplore.ieee.org/abstract/document/5963691) | 2009 | Influential analysis explaining why many blind deblurring methods fail and clarifying the role of MAP estimation. |
| Fast Image Deconvolution using Hyper-Laplacian Priors (Krishnan & Fergus) | [Link](https://proceedings.neurips.cc/paper_files/paper/2009/hash/3dd48ab31d016ffcbf3314df2b3cb9ce-Abstract.html) | 2009 | Introduces hyper-Laplacian gradient priors for efficient non-blind deconvolution. |
| Blind Deconvolution using a Normalized Sparsity Measure (Krishnan et al.) | [Link](https://ieeexplore.ieee.org/document/5995521/) | 2011 | Proposes a normalized sparsity measure ($\ell_1/\ell_2$) that improves kernel estimation in blind deblurring. |

---

## Deep Learning Deblurring

| Title | Link | Year | Description |
|------|------|------|-------------|
| Learning a Convolutional Neural Network for Non-uniform Motion Blur Removal (Sun et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2015/html/Sun_Learning_a_Convolutional_2015_CVPR_paper.html) | 2015 | Early CNN approach that predicts motion blur kernels from image patches. |
| Deep Multi-Scale CNN for Dynamic Scene Deblurring (Nah et al.) | [Link](https://openaccess.thecvf.com/content_cvpr_2017/html/Nah_Deep_Multi-Scale_Convolutional_CVPR_2017_paper.html) | 2017 | Introduces a multi-scale CNN architecture and the GoPro dataset; widely considered the start of modern deep deblurring. |
| DeblurGAN: Blind Motion Deblurring Using Conditional Adversarial Networks (Kupyn et al.) | [Link](https://openaccess.thecvf.com/content_cvpr_2018/html/Kupyn_DeblurGAN_Blind_Motion_CVPR_2018_paper.html) | 2018 | Applies GANs to deblurring to improve perceptual image quality. |
| Scale-Recurrent Network for Deep Image Deblurring (Tao et al.) | [Link](http://openaccess.thecvf.com/content_cvpr_2018/html/Tao_Scale-Recurrent_Network_for_CVPR_2018_paper.html) | 2018 | Introduces a recurrent multi-scale architecture for dynamic scene deblurring. |
| DeblurGAN-v2: Deblurring (Orders-of-Magnitude) Faster and Better(Kupyn et al.) | [Link](https://openaccess.thecvf.com/content_ICCV_2019/html/Kupyn_DeblurGAN-v2_Deblurring_Orders-of-Magnitude_Faster_and_Better_ICCV_2019_paper.html) | 2019 | Faster and more accurate GAN-based deblurring with feature pyramid networks. |
| MPRNet: Multi-Stage Progressive Image Restoration (Zamir et al.) | [Link](https://openaccess.thecvf.com/content/CVPR2021/html/Zamir_Multi-Stage_Progressive_Image_Restoration_CVPR_2021_paper.html) | 2021 | Multi-stage architecture with an encoder-decoder structure that achieves strong results across several restoration tasks including deblurring. |
| Restormer: Efficient Transformer for High-Resolution Image Restoration (Zamir et al.) | [Link](https://openaccess.thecvf.com/content/CVPR2022/html/Zamir_Restormer_Efficient_Transformer_for_High-Resolution_Image_Restoration_CVPR_2022_paper.html) | 2022 | Transformer-based architecture designed for high-resolution restoration tasks including deblurring. |

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| GoPro (Nah et al.) | [Link](https://github.com/SeungjunNah/DeepDeblur_release) | 3,214 blurry/sharp pairs synthesized from high-speed video; the de facto standard benchmark for dynamic motion deblurring. |
| HIDE (Shen et al.) | [Link](https://github.com/joanshen0508/HA_deblur) | Human-aware motion blur dataset; used primarily for generalization evaluation of models trained on GoPro. |
| RealBlur (Rim et al.) | [Link](https://github.com/rimchang/RealBlur) | Real blurry/sharp image pairs captured simultaneously with a beam-splitter rig; benchmark for evaluating on genuine optical blur. |
| Köhler Dataset | [Link](https://webdav.tuebingen.mpg.de/pixel/benchmark4camerashake/) | 48 real blurry images with ground truth sharp images and kernels; classic benchmark for blind deblurring with known reference. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| Restormer (official) | [Link](https://github.com/swz30/Restormer) | Official PyTorch implementation of Restormer; includes pretrained models and evaluation scripts for GoPro and RealBlur. |
| MPRNet (official) | [Link](https://github.com/swz30/MPRNet) | Official implementation of MPRNet; strong multi-stage baseline for motion deblurring with pretrained weights. |
| DeblurGAN-v2 (official) | [Link](https://github.com/VITA-Group/DeblurGANv2) | Official implementation of DeblurGAN-v2 for blind motion deblurring using GANs. |
| BasicSR | [Link](https://github.com/XPixelGroup/BasicSR) | General image restoration framework with training pipelines for multiple deblurring methods. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../../CONTRIBUTING.md) before submitting.
