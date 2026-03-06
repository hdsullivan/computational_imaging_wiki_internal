---
title: Phase Retrieval
nav_order: 3
---

# Phase Retrieval

Phase retrieval is the problem of recovering a signal from measurements of its Fourier magnitude (or more generally, from phaseless measurements), where the phase information is lost during acquisition. It arises naturally in X-ray crystallography, coherent diffractive imaging, and optical imaging systems where only intensity — not the complex field — can be recorded. The field spans classical iterative projection algorithms, convex relaxation methods, and modern learning-based approaches.

---

## Foundational & Highly Cited Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Phase Retrieval Algorithms: A Comparison (Fienup) | [Link](https://opg.optica.org/ao/abstract.cfm?uri=ao-21-15-2758) | 1982 | Classic paper comparing iterative phase retrieval algorithms (error-reduction, hybrid input-output) that remain widely used today. |
| Phase Retrieval via Matrix Completion (Candes et al.) | [Link](https://arxiv.org/abs/0909.3535) | 2011 | Introduces PhaseLift, a convex relaxation of phase retrieval via semidefinite programming with provable recovery guarantees. |
| Solving Systems of Random Quadratic Equations via Truncated Amplitude Flow (Wirtinger Flow) (Candes et al.) | [Link](https://arxiv.org/abs/1407.1065) | 2015 | Provides the first provably efficient non-convex algorithm (Wirtinger Flow) for phase retrieval from Gaussian measurements. |
| Solving Random Systems of Quadratic Equations via Truncated Generalized Gradient Flow (Zhang et al.) | [Link](https://arxiv.org/abs/1612.03652) | 2016 | Truncated amplitude flow, improving on Wirtinger Flow with better sample complexity and empirical performance. |
| Deep Phase Decoder: Self-Calibrating Phase Microscopy with an Untrained Deep Neural Network (Bostan et al.) | [Link](https://arxiv.org/abs/2004.00660) | 2020 | Demonstrates that untrained deep networks (deep image prior) can serve as effective priors for phase retrieval in microscopy. |
| prDeep: Robust Phase Retrieval with a Flexible Deep Network Prior (Metzler et al.) | [Link](https://arxiv.org/abs/1803.00212) | 2018 | Applies plug-and-play priors with a learned denoiser to phase retrieval, bridging iterative and learning-based approaches. |

---

## Datasets

| Title | Link | Description |
|-------|------|-------------|
| CXIDB (Coherent X-ray Imaging Data Bank) | [Link](https://www.cxidb.org/) | Repository of experimental coherent X-ray diffraction imaging datasets contributed by the community. |
| Phase Retrieval Benchmark (Sfard et al.) | [Link](https://github.com/talsf/PhaseRetrieval-benchmark) | Standardized benchmark suite for evaluating phase retrieval algorithms on simulated and real optical datasets. |

---

## Code & Software

| Title | Link | Description |
|-------|------|-------------|
| PhasePack | [Link](https://github.com/tomgoldstein/phasepack-matlab) | MATLAB library implementing many classical and modern phase retrieval algorithms with a unified interface for benchmarking. |
| PtyPy (Ptychography Package) | [Link](https://github.com/ptycho/ptypy) | Python framework for ptychographic phase retrieval, supporting multiple engines and experimental geometries. |
| PhaseStudio | [Link](https://github.com/IgorCATech/PhaseStudio) | Python toolkit for phase retrieval in optical and X-ray imaging, with support for iterative projection algorithms. |
| HIO / ER Reference Implementation | [Link](https://github.com/siddharth-maddali/Phaser) | Python implementation of error-reduction and hybrid input-output algorithms for Bragg coherent diffractive imaging. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../CONTRIBUTING.md) before submitting.
