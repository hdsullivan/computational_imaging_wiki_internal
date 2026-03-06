---
title: Classical Algorithms
parent: Phase Retrieval
nav_order: 1
---

# Classical Algorithms

{: .important }
> Papers listed here should be **seminal, widely cited, or game-changing**. See the [Contribution Guide](../../contributing/) for the full criteria before submitting.

## 📄 Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Phase Retrieval Algorithms: A Comparison (Fienup) | [Link](https://opg.optica.org/ao/abstract.cfm?uri=ao-21-15-2758) | 1982 | Classic paper comparing iterative phase retrieval algorithms (error-reduction, hybrid input-output) that remain widely used today. |
| Solving Systems of Random Quadratic Equations via Truncated Amplitude Flow — Wirtinger Flow (Candes et al.) | [Link](https://arxiv.org/abs/1407.1065) | 2015 | Provides the first provably efficient non-convex algorithm (Wirtinger Flow) for phase retrieval from Gaussian measurements. |
| Solving Random Systems of Quadratic Equations via Truncated Generalized Gradient Flow (Zhang et al.) | [Link](https://arxiv.org/abs/1612.03652) | 2016 | Truncated amplitude flow, improving on Wirtinger Flow with better sample complexity and empirical performance. |

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| CXIDB (Coherent X-ray Imaging Data Bank) | [Link](https://www.cxidb.org/) | Repository of experimental coherent X-ray diffraction imaging datasets; primary source for real CDI phase retrieval data. |
| Phase Retrieval Benchmark (Sfard et al.) | [Link](https://github.com/talsf/PhaseRetrieval-benchmark) | Standardized benchmark suite for evaluating classical and modern phase retrieval algorithms. |

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| PhasePack | [Link](https://github.com/tomgoldstein/phasepack-matlab) | MATLAB library implementing HIO, Wirtinger Flow, and many other classical phase retrieval algorithms with a unified interface. |
| HIO / ER Reference Implementation (Phaser) | [Link](https://github.com/siddharth-maddali/Phaser) | Python implementation of error-reduction and hybrid input-output for Bragg coherent diffractive imaging. |
