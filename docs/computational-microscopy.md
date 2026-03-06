---
title: Computational Microscopy
nav_order: 5
---

# Computational Microscopy

Computational microscopy combines optical hardware design with advanced algorithms to overcome the resolution, throughput, and depth limits of conventional microscopy. By jointly designing the acquisition process and the reconstruction algorithm, it enables imaging beyond the classical diffraction limit, three-dimensional reconstruction from two-dimensional measurements, and quantitative phase imaging of transparent specimens. Key techniques include Fourier ptychography, structured illumination, light field microscopy, and neural-network-enhanced microscopy.

---

## 📄 Papers


{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing** — work the community broadly recognizes as essential reading. See the [Contribution Guide](/contributing/) for the full criteria.

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Fourier Ptychographic Microscopy (Zheng et al.) | [Link](https://www.nature.com/articles/nphoton.2013.187) | 2013 | Introduces FPM, a computational technique achieving gigapixel imaging and quantitative phase recovery using angle-varied LED illumination. |
| Deep Learning Microscopy (Rivenson et al.) | [Link](https://arxiv.org/abs/1705.04709) | 2017 | Demonstrates that deep neural networks can enhance the resolution and quality of fluorescence microscopy images. |
| Content-Aware Image Restoration: Pushing the Limits of Fluorescence Microscopy (CARE) (Weigert et al.) | [Link](https://www.nature.com/articles/s41592-018-0216-7) | 2018 | Proposes content-aware restoration networks trained on paired low/high-quality data for fluorescence microscopy. |
| Learned Large Field-of-View Imaging with Thin-Plate Optics (Peng et al.) | [Link](https://arxiv.org/abs/1909.06223) | 2019 | Joint design of optics and reconstruction network for large field-of-view computational imaging. |
| Physics-Enhanced Deep Neural Network for Optical Diffraction Tomography (Chen et al.) | [Link](https://arxiv.org/abs/2112.01891) | 2022 | Combines physical forward models with deep learning for 3D refractive index reconstruction from diffraction measurements. |
| Three-Dimensional Fluorescence Microscopy with Adaptive Optics for Biology (Booth) | [Link](https://royalsocietypublishing.org/doi/10.1098/rsta.2014.0230) | 2014 | Review of adaptive optics techniques for correcting aberrations and recovering resolution in deep-tissue fluorescence microscopy. |

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Cell Image Library | [Link](http://www.cellimagelibrary.org/) | Public repository of cellular and subcellular microscopy images across modalities and organisms. |
| BioSR (Biological Super-Resolution) | [Link](https://figshare.com/articles/dataset/BioSR/13264793) | Paired diffraction-limited and super-resolution fluorescence microscopy images for benchmarking restoration methods. |
| DeepLoco Dataset | [Link](https://github.com/EliasNehme/DeepLoco) | Single-molecule localization microscopy data for benchmarking 3D SMLM reconstruction algorithms. |
| OpenCell | [Link](https://opencell.czbiohub.org/) | Large-scale fluorescence microscopy dataset of endogenously tagged human proteins across hundreds of cell lines. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| PtyPy | [Link](https://github.com/ptycho/ptypy) | Python framework for ptychographic reconstruction, supporting multiple engines and both optical and X-ray geometries. |
| CARE (Content-Aware Image Restoration) | [Link](https://github.com/CSBDeep/CSBDeep) | Python/Keras library for training and applying deep learning models for fluorescence microscopy restoration. |
| ThunderSTORM | [Link](https://github.com/zitmen/thunderstorm) | ImageJ plugin for single-molecule localization microscopy (SMLM) data analysis and super-resolution reconstruction. |
| microDL | [Link](https://github.com/mehta-lab/microDL) | PyTorch framework for deep learning in computational microscopy, supporting virtual staining and phase imaging tasks. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](/contributing/) before submitting.
