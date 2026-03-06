---
title: Neural Radiance Fields (NeRF)
parent: Neural Scene Representation
nav_order: 1
---

# Neural Radiance Fields (NeRF)

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis (Mildenhall et al.) | [Link](https://arxiv.org/abs/2003.08934) | 2020 | Introduces Neural Radiance Fields, enabling photorealistic novel view synthesis from a sparse set of posed images using a simple MLP. |
| Mip-NeRF 360: Unbounded Anti-Aliased Neural Radiance Fields (Barron et al.) | [Link](https://arxiv.org/abs/2111.12077) | 2022 | Extends NeRF to unbounded 360° scenes with anti-aliasing, setting strong benchmarks for novel view synthesis quality. |
| Instant Neural Graphics Primitives with a Multiresolution Hash Encoding (Müller et al.) | [Link](https://arxiv.org/abs/2201.05989) | 2022 | Proposes a multiresolution hash encoding that reduces NeRF training from hours to seconds while maintaining quality. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| NeRF Synthetic Dataset (Blender) | [Link](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1) | Eight synthetic objects with 100 views each; the standard benchmark introduced with the original NeRF paper. |
| Mip-NeRF 360 Dataset | [Link](https://jonbarron.info/mipnerf360/) | Real unbounded indoor and outdoor scenes; the standard benchmark for evaluating novel view synthesis quality. |
| LLFF (Local Light Field Fusion) | [Link](https://github.com/Fyusion/LLFF) | Forward-facing real scene captures widely used for evaluating NeRF variants on bounded scenes. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| nerfstudio | [Link](https://github.com/nerfstudio-project/nerfstudio) | Modular PyTorch framework for training, visualizing, and exporting NeRF and related models. |
| Instant-NGP | [Link](https://github.com/NVlabs/instant-ngp) | NVIDIA's CUDA implementation of multiresolution hash encoding for near-instant NeRF training. |
