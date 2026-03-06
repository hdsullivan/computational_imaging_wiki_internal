---
title: Image Restoration
nav_order: 3
has_children: true
---

# Image Restoration

Image restoration covers algorithms for restoring or enhancing images that have been degraded by noise, blur, downsampling, or other acquisition artifacts. The field includes classical problems — denoising, deblurring, super-resolution, inpainting — and increasingly addresses these jointly or as special cases of inverse problems. Deep learning has dramatically advanced the state of the art, with architectures ranging from CNNs and transformers to diffusion models.

Browse papers by sub-topic using the sidebar, or jump directly to:
[Denoising](image-reconstruction/denoising) · [Deblurring](image-reconstruction/deblurring) · [Super-Resolution](image-reconstruction/super-resolution) · [Diffusion-Based Restoration](image-reconstruction/diffusion-based-restoration)

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
| OpenMMLab mmagic | [Link](https://github.com/open-mmlab/mmagic) | OpenMMLab's image/video restoration and generation library, supporting super-resolution, denoising, inpainting, and more. |
| Diffusers (HuggingFace) | [Link](https://github.com/huggingface/diffusers) | Widely used library for diffusion models; relevant for diffusion-based image restoration and inverse problem solving. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
