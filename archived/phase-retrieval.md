---
title: Phase Retrieval
nav_order: 3
has_children: true
---

# Phase Retrieval

Phase retrieval is the problem of recovering a signal from measurements of its Fourier magnitude (or more generally, from phaseless measurements), where the phase information is lost during acquisition. It arises naturally in X-ray crystallography, coherent diffractive imaging, and optical imaging systems where only intensity — not the complex field — can be recorded. The field spans classical iterative projection algorithms, convex relaxation methods, and modern learning-based approaches.

Browse papers by sub-topic using the sidebar, or jump directly to:
[Classical Algorithms](phase-retrieval/classical-algorithms) · [Convex Relaxation](phase-retrieval/convex-relaxation) · [Deep Learning Approaches](phase-retrieval/deep-learning)

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| CXIDB (Coherent X-ray Imaging Data Bank) | [Link](https://www.cxidb.org/) | Repository of experimental coherent X-ray diffraction imaging datasets contributed by the community. |
| Phase Retrieval Benchmark (Sfard et al.) | [Link](https://github.com/talsf/PhaseRetrieval-benchmark) | Standardized benchmark suite for evaluating phase retrieval algorithms on simulated and real optical datasets. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| PhasePack | [Link](https://github.com/tomgoldstein/phasepack-matlab) | MATLAB library implementing many classical and modern phase retrieval algorithms with a unified interface for benchmarking. |
| PtyPy (Ptychography Package) | [Link](https://github.com/ptycho/ptypy) | Python framework for ptychographic phase retrieval, supporting multiple engines and experimental geometries. |
| PhaseStudio | [Link](https://github.com/IgorCATech/PhaseStudio) | Python toolkit for phase retrieval in optical and X-ray imaging, with support for iterative projection algorithms. |
| HIO / ER Reference Implementation | [Link](https://github.com/siddharth-maddali/Phaser) | Python implementation of error-reduction and hybrid input-output algorithms for Bragg coherent diffractive imaging. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.
