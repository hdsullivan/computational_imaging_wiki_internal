---
title: Neural Scene Representation
nav_order: 6
has_children: true
---

# Neural Scene Representation

Neural scene representations encode 3D scenes — geometry, appearance, and lighting — as the weights of a neural network or as neural fields, rather than in explicit geometric structures like meshes or voxels. The field has grown rapidly since NeRF (2020), with methods enabling photorealistic novel view synthesis, 3D reconstruction from sparse images, and editable scene representations.

Browse papers by sub-topic using the sidebar, or jump directly to:
[Neural Radiance Fields](neural-scene-representation/nerf) · [Gaussian Splatting](neural-scene-representation/gaussian-splatting) · [Implicit Neural Surfaces](neural-scene-representation/implicit-surfaces)

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| NeRF Synthetic Dataset (Blender) | [Link](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1) | Eight synthetic objects with 100 views each; the standard benchmark introduced with the original NeRF paper. |
| Tanks and Temples | [Link](https://www.tanksandtemples.org/) | Real-world benchmark for large-scale 3D reconstruction from video, with lidar ground truth for evaluation. |
| Mip-NeRF 360 Dataset | [Link](https://jonbarron.info/mipnerf360/) | Unbounded real indoor and outdoor scenes used as benchmarks for novel view synthesis quality. |
| DTU MVS Dataset | [Link](https://roboimagedata.compute.dtu.dk/?page_id=36) | Multi-view stereo benchmark with structured-light ground truth, widely used to evaluate neural surface reconstruction. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| nerfstudio | [Link](https://github.com/nerfstudio-project/nerfstudio) | Modular PyTorch framework for training, visualizing, and exporting NeRF and Gaussian Splatting models. |
| 3D Gaussian Splatting (official) | [Link](https://github.com/graphdeco-inria/gaussian-splatting) | Official implementation of 3D Gaussian Splatting for real-time radiance field rendering. |
| Instant-NGP | [Link](https://github.com/NVlabs/instant-ngp) | NVIDIA's CUDA implementation of multiresolution hash encoding for instant NeRF training and inference. |
| NeuS (official) | [Link](https://github.com/Totoro97/NeuS) | Official implementation of NeuS neural implicit surface reconstruction. |
| sdfstudio | [Link](https://github.com/autonomousvision/sdfstudio) | Unified framework for neural implicit surface reconstruction methods, built on nerfstudio. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
