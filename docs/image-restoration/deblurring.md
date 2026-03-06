---
title: Deblurring
parent: Image Reconstruction
nav_order: 2
---

# Deblurring

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Image Restoration Using Very Deep Convolutional Encoder-Decoder Networks (RED-Net) (Mao et al.) | [Link](https://arxiv.org/abs/1603.09056) | 2016 | Deep encoder-decoder with symmetric skip connections for image denoising and deblurring. |
| Restormer: Efficient Transformer for High-Resolution Image Restoration (Zamir et al.) | [Link](https://arxiv.org/abs/2111.09881) | 2022 | Hierarchical transformer architecture achieving state-of-the-art results across denoising, motion deblurring, and deraining. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| GoPro Dataset (Nah et al.) | [Link](https://github.com/SeungjunNah/DeepDeblur_release) | 3,214 blurry/sharp image pairs generated from high-speed video; standard benchmark for dynamic motion deblurring. |
| HIDE Dataset | [Link](https://github.com/joanshen0508/HA_deblur) | Motion blur dataset focused on human-aware deblurring with people in scenes. |
| RealBlur Dataset | [Link](https://github.com/rimchang/RealBlur) | Real-world blurry/sharp image pairs captured with a beam-splitter rig; benchmark for realistic deblurring evaluation. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| Restormer (official) | [Link](https://github.com/swz30/Restormer) | Official PyTorch implementation of Restormer for motion deblurring, denoising, and deraining. |
| DeblurGAN-v2 | [Link](https://github.com/VITA-Group/DeblurGANv2) | GAN-based deblurring model with strong perceptual quality on real motion blur. |
| MPRNet | [Link](https://github.com/swz30/MPRNet) | Multi-stage progressive restoration network; strong baseline for deblurring, denoising, and deraining. |
