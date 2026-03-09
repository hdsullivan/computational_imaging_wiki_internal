---
title: Diffusion-Based Restoration
parent: Image Restoration
nav_order: 4
---

# Diffusion-Based Restoration

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Denoising Diffusion Probabilistic Models (Ho et al.) | [Link](https://arxiv.org/abs/2006.11239) | 2020 | Introduces DDPMs, establishing the foundation for applying diffusion models to image synthesis and, subsequently, restoration. |
| Palette: Image-to-Image Diffusion Models (Saharia et al.) | [Link](https://arxiv.org/abs/2111.05826) | 2022 | Applies a single conditional diffusion model to four image restoration tasks (denoising, inpainting, colorization, JPEG restoration). |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| FFHQ (Flickr-Faces-HQ) | [Link](https://github.com/NVlabs/ffhq-dataset) | 70,000 high-quality face images; widely used for evaluating diffusion-based face restoration and super-resolution. |
| ImageNet | [Link](https://www.image-net.org/) | Large-scale visual database used for training and evaluating diffusion models and general image restoration methods. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| Diffusers (HuggingFace) | [Link](https://github.com/huggingface/diffusers) | Widely used library for diffusion models; supports DDPM, DDIM, and many variants for image generation and restoration. |
| guided-diffusion (OpenAI) | [Link](https://github.com/openai/guided-diffusion) | Official implementation of ADM, a strong baseline diffusion model used in many downstream restoration works. |


{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](CONTRIBUTING.md) before submitting.
