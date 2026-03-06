---
title: Medical Imaging
nav_order: 7
---

# Medical Imaging

Medical imaging encompasses the computational methods for acquiring, reconstructing, and analyzing images from clinical modalities including MRI, CT, ultrasound, and PET. Key challenges include accelerated acquisition (fewer measurements, faster scans), artifact removal, segmentation of anatomical structures, and the integration of prior knowledge — both physical and learned — into reconstruction pipelines. Deep learning has had a particularly large impact here, enabling both faster reconstruction and improved diagnostic image quality.

---

## Foundational & Highly Cited Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| U-Net: Convolutional Networks for Biomedical Image Segmentation (Ronneberger et al.) | [Link](https://arxiv.org/abs/1505.04597) | 2015 | Proposes the U-Net encoder-decoder architecture with skip connections, which became the dominant model for medical image segmentation. |
| Sparse MRI: The Application of Compressed Sensing for Rapid MR Imaging (Lustig et al.) | [Link](https://onlinelibrary.wiley.com/doi/10.1002/mrm.21391) | 2007 | First major paper applying compressed sensing to accelerate MRI acquisition by exploiting image sparsity. |
| Deep Learning for Accelerated MRI (Yang et al.) | [Link](https://arxiv.org/abs/1706.07519) | 2017 | Introduces ADMM-Net, an early deep unrolling approach for accelerated MRI reconstruction from undersampled k-space. |
| End-to-End Variational Networks for Accelerated MRI Reconstruction (Sriram et al.) | [Link](https://arxiv.org/abs/2004.06688) | 2020 | Proposes a deep cascade of variational networks for MRI reconstruction; top performer in the fastMRI challenge. |
| nnU-Net: A Self-Configuring Method for Deep Learning-Based Biomedical Image Segmentation (Isensee et al.) | [Link](https://arxiv.org/abs/1809.10486) | 2021 | Presents an automatically configuring U-Net framework that achieved state-of-the-art segmentation across a wide range of tasks. |
| Score-Based Diffusion Models for Accelerated MRI (Chung & Ye) | [Link](https://arxiv.org/abs/2110.05243) | 2022 | Applies diffusion model priors to accelerated MRI reconstruction, enabling high-quality recovery at high acceleration factors. |

---

## Datasets

| Title | Link | Description |
|-------|------|-------------|
| fastMRI (Facebook AI / NYU) | [Link](https://fastmri.org/) | Large-scale dataset of raw MRI k-space data for benchmarking accelerated reconstruction methods; includes brain and knee scans. |
| Medical Segmentation Decathlon | [Link](http://medicaldecathlon.com/) | Ten-task segmentation challenge covering organs and tumors across MRI and CT modalities with diverse annotation styles. |
| TCIA (The Cancer Imaging Archive) | [Link](https://www.cancerimagingarchive.net/) | Large public repository of de-identified cancer medical images including CT, MRI, and pathology. |
| IXI Dataset | [Link](https://brain-development.org/ixi-dataset/) | MRI brain images from nearly 600 healthy subjects, used for registration, segmentation, and reconstruction research. |
| LIDC-IDRI (Lung Image Database Consortium) | [Link](https://www.cancerimagingarchive.net/collection/lidc-idri/) | CT scans of the chest with expert radiologist annotations of lung nodules, a standard benchmark for detection. |

---

## Code & Software

| Title | Link | Description |
|-------|------|-------------|
| MONAI (Medical Open Network for AI) | [Link](https://github.com/Project-MONAI/MONAI) | PyTorch-based framework for deep learning in medical imaging, covering segmentation, reconstruction, and registration. |
| fastMRI (Facebook Research) | [Link](https://github.com/facebookresearch/fastMRI) | PyTorch codebase and baseline models for the fastMRI accelerated MRI reconstruction challenge. |
| SimpleITK | [Link](https://github.com/SimpleITK/SimpleITK) | Widely used Python/C++ toolkit for reading, writing, and processing medical images across formats (DICOM, NIfTI, etc.). |
| TorchIO | [Link](https://github.com/fepegar/torchio) | PyTorch library for efficient loading, preprocessing, and augmentation of 3D medical images. |
| SigPy | [Link](https://github.com/mikgroup/sigpy) | Python library for MRI signal processing and reconstruction, with support for parallel imaging and compressed sensing. |

---

*To add an entry, see [CONTRIBUTING.md](../CONTRIBUTING.md).*
