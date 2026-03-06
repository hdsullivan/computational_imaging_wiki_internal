---
title: Segmentation
parent: Medical Imaging
nav_order: 2
---

# Segmentation

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| U-Net: Convolutional Networks for Biomedical Image Segmentation (Ronneberger et al.) | [Link](https://arxiv.org/abs/1505.04597) | 2015 | Proposes the U-Net encoder-decoder architecture with skip connections, which became the dominant model for medical image segmentation. |
| nnU-Net: A Self-Configuring Method for Deep Learning-Based Biomedical Image Segmentation (Isensee et al.) | [Link](https://arxiv.org/abs/1809.10486) | 2021 | Automatically configuring U-Net framework that achieved state-of-the-art segmentation across a wide range of medical imaging tasks. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Medical Segmentation Decathlon | [Link](http://medicaldecathlon.com/) | Ten-task challenge covering organ and tumor segmentation across MRI and CT with diverse annotation styles. |
| TCIA (The Cancer Imaging Archive) | [Link](https://www.cancerimagingarchive.net/) | Large public repository of de-identified cancer images with annotations for segmentation and detection tasks. |
| LIDC-IDRI | [Link](https://www.cancerimagingarchive.net/collection/lidc-idri/) | CT scans with expert radiologist annotations of lung nodules; standard benchmark for pulmonary nodule detection and segmentation. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| MONAI (Medical Open Network for AI) | [Link](https://github.com/Project-MONAI/MONAI) | PyTorch framework for medical image analysis including segmentation, with U-Net variants and training utilities. |
| nnU-Net (official) | [Link](https://github.com/MIC-DKFZ/nnUNet) | Official implementation of nnU-Net; the go-to baseline for medical image segmentation across modalities. |
