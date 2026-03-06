---
title: Gaussian Splatting
parent: Neural Scene Representation
nav_order: 2
---

# Gaussian Splatting

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| 3D Gaussian Splatting for Real-Time Radiance Field Rendering (Kerbl et al.) | [Link](https://arxiv.org/abs/2308.04079) | 2023 | Represents scenes as explicit 3D Gaussians, enabling real-time novel view synthesis and significantly faster optimization than NeRF. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Tanks and Temples | [Link](https://www.tanksandtemples.org/) | Real-world benchmark for large-scale 3D reconstruction from video, with lidar ground truth for evaluation. |
| Mip-NeRF 360 Dataset | [Link](https://jonbarron.info/mipnerf360/) | Unbounded real scenes used as a primary benchmark for Gaussian splatting rendering quality comparisons. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| 3D Gaussian Splatting (official) | [Link](https://github.com/graphdeco-inria/gaussian-splatting) | Official CUDA implementation of 3DGS for real-time radiance field rendering. |
| nerfstudio | [Link](https://github.com/nerfstudio-project/nerfstudio) | Includes Gaussian Splatting support alongside NeRF variants in a unified training framework. |
