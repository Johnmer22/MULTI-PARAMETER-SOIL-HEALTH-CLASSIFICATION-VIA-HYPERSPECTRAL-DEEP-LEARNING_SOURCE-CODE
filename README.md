# MULTI-PARAMETER SOIL HEALTH CLASSIFICATION VIA HYPERSPECTRAL DEEP LEARNING: ADVANCING PRECISION AGRICULTURE THROUGH NON-INVASIVE NUTRIENT AND CONTAMINANT DETECTION

## Project Overview
[cite_start]This repository contains the official implementation of the **6-Head Hybrid 1D-CNN-BiLSTM-Attention Model**, a custom deep learning framework designed for non-invasive soil health assessment[cite: 128, 192]. [cite_start]The model simultaneously classifies primary agronomic macronutrients (Total Nitrogen, Soil Organic Carbon, Extractable Potassium) into three actionable management tiers, while concurrently executing binary toxicity screening for persistent heavy metals (Lead, Arsenic, Cadmium)[cite: 193, 198].

[cite_start]To overcome the inherent environmental data scarcity paradox associated with physical toxic sampling, this framework utilizes a **Physics-Informed "Digital Spiking" Strategy**[cite: 185, 194, 196]. [cite_start]By anchoring the data pipeline on the Beer-Lambert Law and the Linear Mixing Model (LMM), theoretical trace contaminant signatures are mathematically superimposed onto 19,807 globally diverse soil backgrounds sourced from the Open Soil Spectral Library (OSSL)[cite: 130, 197].

---

## Core Technical Features
* [cite_start]**Programmatic Dataset Harmonization:** Automated relational one-to-one inner join utilizing the OSSL standardized primary key (`id.layer_uuid_txt`) to perfectly intersect continuous Vis-NIR-SWIR spectral bands (400–2500 nm) with wet-chemistry ground truth labels[cite: 228, 405, 406, 407].
* [cite_start]**Physics-Informed Augmentation (Digital Spiking Engine):** Simulates trace contamination profiles at an absorption scaling factor of $\alpha = 0.1$ (10% signal power) embedded under an explicitly injected $\sigma = 0.05$ (5% stochastic noise) boundary layer to replicate chaotic real-world sensor drift[cite: 439, 446, 456, 686].
* **Custom 6-Head Multi-Task Topology:**
  * [cite_start]**1D-CNN Blocks:** Act as high-dimensional spatial morphological edge and curve shape detectors to capture local absorption bands[cite: 361, 502, 504].
  * [cite_start]**Bidirectional LSTMs:** Process the continuous spectrum as sequential waves (both 400→2500nm and 2500→400nm) to actively isolate and filter out environmental moisture baseline drift[cite: 294, 512, 513].
  * [cite_start]**Custom Attention Layer:** Dynamically calculates soft-weight importance vectors to prioritize target molecular overtones (C-H, N-H bonds) while forcefully suppressing overwhelming iron-oxide spectral masking[cite: 268, 297, 298, 526, 527].

---
