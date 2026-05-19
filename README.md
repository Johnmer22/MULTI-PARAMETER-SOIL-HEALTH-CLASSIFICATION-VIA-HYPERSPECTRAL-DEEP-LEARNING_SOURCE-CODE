# MULTI-PARAMETER SOIL HEALTH CLASSIFICATION VIA HYPERSPECTRAL DEEP LEARNING: ADVANCING PRECISION AGRICULTURE THROUGH NON-INVASIVE NUTRIENT AND CONTAMINANT DETECTION

## Project Overview
This repository contains the official implementation of the **6-Head Hybrid 1D-CNN-BiLSTM-Attention Model**, a custom deep learning framework designed for non-invasive soil health assessment.The model simultaneously classifies primary agronomic macronutrients (Total Nitrogen, Soil Organic Carbon, Extractable Potassium) into three actionable management tiers, while concurrently executing binary toxicity screening for persistent heavy metals (Lead, Arsenic, Cadmium).

To overcome the inherent environmental data scarcity paradox associated with physical toxic sampling, this framework utilizes a **Physics-Informed "Digital Spiking" Strategy**. By anchoring the data pipeline on the Beer-Lambert Law and the Linear Mixing Model (LMM), theoretical trace contaminant signatures are mathematically superimposed onto 19,807 globally diverse soil backgrounds sourced from the Open Soil Spectral Library (OSSL).

---

## Core Technical Features
**Programmatic Dataset Harmonization:** Automated relational one-to-one inner join utilizing the OSSL standardized primary key (`id.layer_uuid_txt`) to perfectly intersect continuous Vis-NIR-SWIR spectral bands (400–2500 nm) with wet-chemistry ground truth labels.

**Physics-Informed Augmentation (Digital Spiking Engine):** Simulates trace contamination profiles at an absorption scaling factor of $\alpha = 0.1$ (10% signal power) embedded under an explicitly injected $\sigma = 0.05$ (5% stochastic noise) boundary layer to replicate chaotic real-world sensor drift.

**Custom 6-Head Multi-Task Topology:**
* **1D-CNN Blocks:** Act as high-dimensional spatial morphological edge and curve shape detectors to capture local absorption bands.
* **Bidirectional LSTMs:** Process the continuous spectrum as sequential waves (both 400→2500nm and 2500→400nm) to actively isolate and filter out environmental moisture baseline drift.
* **Custom Attention Layer:** Dynamically calculates soft-weight importance vectors to prioritize target molecular overtones (C-H, N-H bonds) while forcefully suppressing overwhelming iron-oxide spectral masking.

---
