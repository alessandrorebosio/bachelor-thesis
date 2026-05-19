# Intelligent Reflecting Surfaces (IRS): Design, Modeling, and Optimization

Thesis repository exploring the control of **Intelligent Reflecting Surfaces (IRS)** using **Machine Learning (ML)** techniques to enhance indoor wireless coverage, particularly for 5G/6G mmWave communications.

## 📝 Overview

Traditional wireless networks focus on optimizing the transmitter and receiver. This project shifts the paradigm by actively reconfiguring the **propagation environment** using IRS—passive, low-cost surfaces with a high number of reflecting elements that can manipulate the phase of incident waves.

Key challenges addressed:
- **Indoor Coverage:** Overcoming penetration loss and "dead zones" in complex indoor environments.
- **mmWave Vulnerability:** Mitigating the high sensitivity of millimeter-wave signals to blockages (NLoS scenarios).
- **Optimization Complexity:** Replacing slow, iterative classical optimization with fast, data-driven ML models.

## 🏗️ Repository Structure

- `analysis.ipynb`: Comprehensive Jupyter notebook containing the dataset generation, ML model implementation, and comparative analysis.
- `docs/`:
    - `thesis.pdf` & `thesis.tex`: Complete thesis documentation (in Italian).
    - `figures/`: Key performance plots and scenario visualizations.
    - `img/`: Project logos and diagrams.
- `slides/`: Gallery of presentation slides summarizing the project.

## 🛰️ System Model & Scenario

The study models a 3D indoor office environment ($10m \times 8m \times 3m$) featuring:
- **Base Station (BS):** Located at $(0, 0, 2.8)m$.
- **IRS:** An $8 \times 8$ grid ($M=64$ elements) at $(9, 4, 1.5)m$.
- **User Equipment (UE):** Mobile user at $z=1m$ within a designated service area.

### Machine Learning Approach
We evaluate three models to predict the optimal IRS phase configuration $\boldsymbol{\theta}$ based on the user's $(x, y)$ position:
1. **Multivariate Linear Regression:** A fast, interpretable baseline.
2. **k-Nearest Neighbors (kNN):** A non-parametric model capturing local spatial dependencies.
3. **Multi-Layer Perceptron (MLP):** A deep learning approach for capturing complex, non-linear relationships.

## 📊 Key Results

The models were evaluated using **Normalized Mean Squared Error (NMSE)** and **Tracking Accuracy** (at $K=4$ phase levels).

- **Quantization Trade-off:** Lower quantization levels ($K=2$) yield higher tracking accuracy (up to 75%), while higher levels ($K=8$) improve phase resolution but increase prediction difficulty.
- **Model Comparison:** MLP and Linear Regression show comparable stability, significantly outperforming random baselines.
- **Coverage Gain:** IRS-assisted links provide substantial SNR improvements in NLoS conditions.

## 🖼️ Presentation Slides

Below is a gallery of the project's presentation slides.

### Title Slide
<p align="center">
  <img src="slides/Intelligent Reflecting Surfaces-1.png" alt="Slide 1" width="700"/>
</p>

### More Slides
<details>
<summary>Click to expand for the full presentation</summary>
<br>

<p align="center">
  <img src="slides/Intelligent Reflecting Surfaces-2.png" alt="Slide 2" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-3.png" alt="Slide 3" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-4.png" alt="Slide 4" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-5.png" alt="Slide 5" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-6.png" alt="Slide 6" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-7.png" alt="Slide 7" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-8.png" alt="Slide 8" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-9.png" alt="Slide 9" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-10.png" alt="Slide 10" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-11.png" alt="Slide 11" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-12.png" alt="Slide 12" width="700"/>
  <img src="slides/Intelligent Reflecting Surfaces-13.png" alt="Slide 13" width="700"/>
</p>
</details>


*Author: Alessandro Rebosio*
*Academic Year: 2025/2026*
