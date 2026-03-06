---
title: Medical Imaging
nav_order: 7
has_children: true
---

# Medical Imaging

Medical imaging encompasses the computational methods for acquiring, reconstructing, and analyzing images from clinical modalities including MRI, CT, ultrasound, and PET. Key challenges include accelerated acquisition, artifact removal, segmentation of anatomical structures, and the integration of prior knowledge — both physical and learned — into reconstruction pipelines.

Browse papers by sub-topic using the sidebar, or jump directly to:
[MRI Reconstruction](medical-imaging/mri-reconstruction) · [Segmentation](medical-imaging/segmentation)

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| fastMRI (Facebook AI / NYU) | [Link](https://fastmri.org/) | Large-scale dataset of raw MRI k-space data for benchmarking accelerated reconstruction methods; includes brain and knee scans. |
| Medical Segmentation Decathlon | [Link](http://medicaldecathlon.com/) | Ten-task segmentation challenge covering organs and tumors across MRI and CT modalities with diverse annotation styles. |
| TCIA (The Cancer Imaging Archive) | [Link](https://www.cancerimagingarchive.net/) | Large public repository of de-identified cancer medical images including CT, MRI, and pathology. |
| IXI Dataset | [Link](https://brain-development.org/ixi-dataset/) | MRI brain images from nearly 600 healthy subjects, used for registration, segmentation, and reconstruction research. |
| LIDC-IDRI (Lung Image Database Consortium) | [Link](https://www.cancerimagingarchive.net/collection/lidc-idri/) | CT scans of the chest with expert radiologist annotations of lung nodules, a standard benchmark for detection. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| MONAI (Medical Open Network for AI) | [Link](https://github.com/Project-MONAI/MONAI) | PyTorch-based framework for deep learning in medical imaging, covering segmentation, reconstruction, and registration. |
| fastMRI (Facebook Research) | [Link](https://github.com/facebookresearch/fastMRI) | PyTorch codebase and baseline models for the fastMRI accelerated MRI reconstruction challenge. |
| SimpleITK | [Link](https://github.com/SimpleITK/SimpleITK) | Widely used Python/C++ toolkit for reading, writing, and processing medical images across formats (DICOM, NIfTI, etc.). |
| TorchIO | [Link](https://github.com/fepegar/torchio) | PyTorch library for efficient loading, preprocessing, and augmentation of 3D medical images. |
| SigPy | [Link](https://github.com/mikgroup/sigpy) | Python library for MRI signal processing and reconstruction, with support for parallel imaging and compressed sensing. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
