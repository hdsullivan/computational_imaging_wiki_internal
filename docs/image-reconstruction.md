---
title: Image Reconstruction
nav_order: 8
---

# Image Reconstruction

Image reconstruction covers algorithms for restoring or enhancing images that have been degraded by noise, blur, downsampling, or other acquisition artifacts. The field includes classical problems — denoising, deblurring, super-resolution, inpainting — and increasingly addresses these jointly or as special cases of inverse problems. Deep learning has dramatically advanced the state of the art, with architectures ranging from CNNs and transformers to diffusion models.

---

## 📄 Papers


{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing** — work the community broadly recognizes as essential reading. See the [Contribution Guide](../contributing/) for the full criteria.

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Beyond a Gaussian Denoiser: Residual Learning of Deep CNN for Image Denoising (DnCNN) (Zhang et al.) | [Link](https://arxiv.org/abs/1608.03981) | 2017 | Introduces DnCNN, an influential residual learning architecture for Gaussian denoising that also handles blind denoising and JPEG artifact removal. |
| Image Super-Resolution Using Deep Convolutional Networks (SRCNN) (Dong et al.) | [Link](https://arxiv.org/abs/1501.00092) | 2015 | First work applying a deep CNN to single-image super-resolution; foundational to the explosion of DL-based SR methods. |
| Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network (SRGAN) (Ledig et al.) | [Link](https://arxiv.org/abs/1609.04802) | 2017 | Proposes SRGAN, which uses perceptual and adversarial losses to produce perceptually sharp super-resolved images. |
| Image Restoration Using Very Deep Convolutional Encoder-Decoder Networks (RED-Net) (Mao et al.) | [Link](https://arxiv.org/abs/1603.09056) | 2016 | Deep encoder-decoder with symmetric skip connections for image denoising and super-resolution. |
| Denoising Diffusion Probabilistic Models (Ho et al.) | [Link](https://arxiv.org/abs/2006.11239) | 2020 | Introduces DDPMs, establishing the foundation for applying diffusion models to image synthesis and, subsequently, restoration. |
| Restormer: Efficient Transformer for High-Resolution Image Restoration (Zamir et al.) | [Link](https://arxiv.org/abs/2111.09881) | 2022 | Proposes a hierarchical transformer architecture for image restoration that achieves state-of-the-art results across denoising, deblurring, and deraining. |

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| BSD68 / CBSD68 | [Link](https://github.com/clausmichele/CBSD68-dataset) | 68 grayscale/color images from the Berkeley Segmentation Dataset; standard benchmark for Gaussian denoising. |
| Set5 / Set14 | [Link](https://github.com/jbhuang0604/SelfExSR) | Small standard sets for super-resolution evaluation that appear in nearly every SR paper for comparison. |
| DIV2K | [Link](https://data.vision.ee.ethz.ch/cvl/DIV2K/) | 1000 high-resolution images used as training and evaluation data for super-resolution and general restoration. |
| Kodak Lossless True Color Image Suite | [Link](http://r0k.us/graphics/kodak/) | 24 high-quality photographic images widely used as a benchmark for compression, denoising, and restoration methods. |
| SIDD (Smartphone Image Denoising Dataset) | [Link](https://www.eecs.yorku.ca/~kamel/sidd/) | Real noisy image pairs captured on smartphones; benchmark for real-noise denoising beyond synthetic Gaussian noise. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| BasicSR (Basic Super-Resolution) | [Link](https://github.com/XPixelGroup/BasicSR) | PyTorch toolkit for image and video restoration; implements many canonical models (SRCNN, ESRGAN, etc.) with training pipelines. |
| Restormer (official) | [Link](https://github.com/swz30/Restormer) | Official PyTorch implementation of the Restormer transformer for image denoising, motion deblurring, and deraining. |
| DnCNN (official) | [Link](https://github.com/cszn/DnCNN) | Original implementation of DnCNN and related residual denoising networks (FFDNet, IRCNN). |
| OpenMMLab mmediting | [Link](https://github.com/open-mmlab/mmagic) | OpenMMLab's image/video restoration and generation library, supporting super-resolution, denoising, inpainting, and more. |
| Diffusers (HuggingFace) | [Link](https://github.com/huggingface/diffusers) | Widely used library for diffusion models; relevant for diffusion-based image restoration and inverse problem solving. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
