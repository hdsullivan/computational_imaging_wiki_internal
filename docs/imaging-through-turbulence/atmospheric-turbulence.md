---
title: Atmospheric Turbulence
parent: Imaging through Turbulence
nav_order: 2
---

# Atmospheric Turbulence

This area focuses on the degradation of images captured over long atmospheric paths, such as in ground-based astronomy and long-range surveillance. It covers computational methods for restoring sharpness and detail lost to the random fluctuations in the atmosphere's refractive index.

---
## 📄 Papers

### Foundation Papers

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Wave Propagation in a Random Medium | [Link](https://archive.org/details/wavepropagationi0000cher/mode/2up) | 1960 | This classic text lays out the early math for how waves propagate through environments with random refractive index changes. It’s a great historical starting point for understanding how atmospheric turbulence was originally modeled statistically. |
| Wave Propagation in a Turbulent Medium | [Link](https://archive.org/details/tatarski-wave-propagation-in-a-turbulent-medium-1961/mode/2up) | 1961 | Building on those early concepts, this book provides the standard framework for how atmospheric turbulence physically distorts optical waves.  It’s a must-read for getting a firm handle on the math behind Kolmogorov turbulence and its direct effects on light traveling through the atmosphere. |
| The spectrum of turbulence | [Link](https://doi.org/10.1098/rspa.1938.0032) | 1938 | This classic paper explains the underlying connection between the wind changes you feel over time at a single spot and the broader wind patterns spread out across space.  It introduces the concept of "frozen turbulence"—imagining a gust of wind as a fixed, unchanging shape that gets blown along by the breeze—which is a crucial idea for understanding how moving air patterns cause the shimmering and optical distortions we observe in the atmosphere. |

### Modeling & Simulation

| Title | Link | Year | Description |
|-------|------|------|-------------|
| Numerical Simulation of Optical Wave Propagation with Examples in MATLAB | [Link](https://www.spiedigitallibrary.org/ebooks/PM/Numerical-Simulation-of-Optical-Wave-Propagation-with-Examples-in-MATLAB/eISBN-9780819483270/10.1117/3.866274) | 2010 | This practical guide bridges the gap between theoretical Fourier optics and actual computer modeling by walking through detailed MATLAB code examples. It is an invaluable reference for software users and researchers looking to build their own split-step wave propagation simulations to accurately model how light degrades as it travels through atmospheric turbulence. |
| Computationally efficient autoregressive method for generating phase screens with frozen flow and turbulence in optical simulations | [Link](https://doi.org/10.1364/OE.23.033335) | 2015 | This paper introduces a practical, efficient way to simulate atmospheric phase screens that accurately capture both wind-driven "frozen flow" and the random "boiling" of the atmosphere.  It is an incredibly helpful resource for software developers and researchers building optical simulations, providing a straightforward method to generate dynamic, time-evolving screens while avoiding the repeating artifacts common in standard Fourier-based approaches. |
| Experimental verification of the frozen flow atmospheric turbulence assumption with use of astronomical adaptive optics telemetry | [Link](https://doi.org/10.1364/JOSAA.26.000833) | 2009 | This paper analyzes real-world data from telescope adaptive optics systems to prove that the "frozen flow" model of atmospheric turbulence is actually present more than 94% of the time.  It is highly useful if you are developing predictive control algorithms or simulations, as it provides solid observational evidence that modeling atmospheric turbulence as discrete, wind-blown layers is a safe and accurate assumption. |

---
<!-- ---
## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Example Dataset | [Link](https://example.com) | One sentence describing the dataset and why it is a standard benchmark. |

---
## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| Example Repo | [Link](https://github.com/org/repo) | One sentence describing what the software does and why it is widely used. |
| Example Repo | [Link](https://github.com/org/repo) | One sentence describing what the software does and why it is widely used. | -->

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../../CONTRIBUTING.md) before submitting.