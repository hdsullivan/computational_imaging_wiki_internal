---
title: Neural Scene Representation
nav_order: 6
---

# Neural Scene Representation

Neural scene representations encode 3D scenes — geometry, appearance, and lighting — as the weights of a neural network or as neural fields, rather than in explicit geometric structures like meshes or voxels. The field has grown rapidly since NeRF (2020), with methods enabling photorealistic novel view synthesis, 3D reconstruction from sparse images, and editable scene representations. It is closely connected to computational imaging through its reliance on differentiable rendering, inverse problems, and physically-based forward models.

---

## Foundational & Highly Cited Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis (Mildenhall et al.) | [Link](https://arxiv.org/abs/2003.08934) | 2020 | Introduces Neural Radiance Fields, enabling photorealistic novel view synthesis from a sparse set of posed images using a simple MLP. |
| Instant Neural Graphics Primitives with a Multiresolution Hash Encoding (Müller et al.) | [Link](https://arxiv.org/abs/2201.05989) | 2022 | Proposes a multiresolution hash encoding that reduces NeRF training from hours to seconds while maintaining quality. |
| 3D Gaussian Splatting for Real-Time Radiance Field Rendering (Kerbl et al.) | [Link](https://arxiv.org/abs/2308.04079) | 2023 | Represents scenes as 3D Gaussians with explicit attributes, enabling real-time novel view synthesis and fast optimization. |
| Mip-NeRF 360: Unbounded Anti-Aliased Neural Radiance Fields (Barron et al.) | [Link](https://arxiv.org/abs/2111.12077) | 2022 | Extends NeRF to unbounded 360° scenes with anti-aliasing, setting strong benchmarks for novel view synthesis quality. |
| Occupancy Networks: Learning 3D Reconstruction in Function Space (Mescheder et al.) | [Link](https://arxiv.org/abs/1812.03828) | 2019 | Represents 3D geometry as a continuous occupancy function learned by a network, enabling high-resolution mesh reconstruction. |
| NeuS: Learning Neural Implicit Surfaces by Volume Rendering for Multi-View Reconstruction (Wang et al.) | [Link](https://arxiv.org/abs/2106.10689) | 2021 | Combines neural signed distance functions with volume rendering to reconstruct accurate, smooth surfaces from multi-view images. |

---

## Datasets

| Title | Link | Description |
|-------|------|-------------|
| NeRF Synthetic Dataset (Blender) | [Link](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1) | Eight synthetic objects with 100 views each; the standard benchmark introduced with the original NeRF paper. |
| Tanks and Temples | [Link](https://www.tanksandtemples.org/) | Real-world benchmark for large-scale 3D reconstruction from video, with lidar ground truth for evaluation. |
| Mip-NeRF 360 Dataset | [Link](https://jonbarron.info/mipnerf360/) | Unbounded real indoor and outdoor scenes used as benchmarks for novel view synthesis quality. |
| DTU MVS Dataset | [Link](https://roboimagedata.compute.dtu.dk/?page_id=36) | Multi-view stereo benchmark with structured-light ground truth, widely used to evaluate neural surface reconstruction. |

---

## Code & Software

| Title | Link | Description |
|-------|------|-------------|
| nerfstudio | [Link](https://github.com/nerfstudio-project/nerfstudio) | Modular PyTorch framework for training, visualizing, and exporting NeRF and Gaussian Splatting models. |
| 3D Gaussian Splatting (official) | [Link](https://github.com/graphdeco-inria/gaussian-splatting) | Official implementation of 3D Gaussian Splatting for real-time radiance field rendering. |
| Instant-NGP | [Link](https://github.com/NVlabs/instant-ngp) | NVIDIA's CUDA implementation of multiresolution hash encoding for instant NeRF training and inference. |
| NeuS (official) | [Link](https://github.com/Totoro97/NeuS) | Official implementation of NeuS neural implicit surface reconstruction. |
| sdfstudio | [Link](https://github.com/autonomousvision/sdfstudio) | Unified framework for neural implicit surface reconstruction methods, built on nerfstudio. |

---

{: .highlight }
> 💡 **Missing something?** Add a paper, dataset, or code repo in 5 minutes — [see the Contribution Guide](../CONTRIBUTING.md).
