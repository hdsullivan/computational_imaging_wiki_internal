---
title: Implicit Neural Surfaces
parent: Neural Scene Representation
nav_order: 3
---

# Implicit Neural Surfaces

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Occupancy Networks: Learning 3D Reconstruction in Function Space (Mescheder et al.) | [Link](https://arxiv.org/abs/1812.03828) | 2019 | Represents 3D geometry as a continuous occupancy function learned by a network, enabling high-resolution mesh reconstruction. |
| NeuS: Learning Neural Implicit Surfaces by Volume Rendering for Multi-View Reconstruction (Wang et al.) | [Link](https://arxiv.org/abs/2106.10689) | 2021 | Combines neural signed distance functions with volume rendering to reconstruct accurate, smooth surfaces from multi-view images. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| DTU MVS Dataset | [Link](https://roboimagedata.compute.dtu.dk/?page_id=36) | Multi-view stereo benchmark with structured-light ground truth; primary benchmark for neural implicit surface reconstruction. |
| BlendedMVS | [Link](https://github.com/YoYo000/BlendedMVS) | Large-scale multi-view stereo dataset with diverse scenes used to evaluate implicit surface reconstruction methods. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| NeuS (official) | [Link](https://github.com/Totoro97/NeuS) | Official PyTorch implementation of NeuS for neural implicit surface reconstruction from multi-view images. |
| sdfstudio | [Link](https://github.com/autonomousvision/sdfstudio) | Unified framework for neural implicit surface methods built on nerfstudio. |
