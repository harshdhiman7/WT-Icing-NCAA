# Wind Turbine Blade Icing Detection Using Multi-Head Attention-Based Transformer

## Overview

Icing accumulation on wind turbine blades can severely reduce both **power output** and **revenue generation**. While traditional approaches—including sensor-based and model-based detection—depend heavily on domain expertise, data-centric methods offer new potential but face unique challenges, such as maintaining a balanced dataset of normal and abnormal (icing) events.

This research project introduces a novel framework that leverages a **multi-head attention transformer** for effective blade icing detection, outperforming established deep learning baselines.

## Table of Contents

- [Project Description](#project-description)
- [Data Collection](#data-collection)
- [Methodology](#methodology)
  - [Data Preprocessing](#data-preprocessing)
  - [Autoencoder Compression](#autoencoder-compression)
  - [Icing Detection Models](#icing-detection-models)
  - [Bayesian Recommendation Engine](#bayesian-recommendation-engine)
- [Results](#results)
- [How to Use](#how-to-use)
- [Future Work](#future-work)


## Project Description

This project addresses the detection and risk assessment of blade icing in wind turbines by:

- Creating a robust, **data-centric pipeline** that leverages transformer models for sequence prediction.
- Comparing deep learning models—**CNN**, **CNN-LSTM**, and **transformer**—for icing detection.
- Building a **Bayesian inference-based recommendation engine** for conditional risk estimation surrounding control actions during icing events.

## Data Collection

- **Source:** Wind turbines on Hitra Island, Norway.
- **Data:** Supervisory Control and Data Acquisition (SCADA) signals, averaged every 10 minutes.
- **Duration:** 12 months of continuous operation.

## Methodology

### Data Preprocessing

- Collected SCADA data is cleaned and normalized to address missing values and ensure data consistency.
- The dataset is balanced between normal and abnormal (icing) events to enhance generalization.

### Autoencoder Compression

- An **autoencoder** model reduces dimensionality, compressing input features while preserving relevant information.
- This step aids both model performance and computational efficiency.

### Icing Detection Models

Three deep learning architectures are evaluated:

| Model        | Description                                                |
|--------------|-----------------------------------------------------------|
| **CNN**      | Utilizes convolutional layers to capture spatial patterns |
| **CNN-LSTM** | Adds temporal modeling via LSTM layers                    |
| **Transformer (Proposed)** | Employs multi-head attention for capturing complex temporal dynamics |

### Bayesian Recommendation Engine

- Based on **Bayesian inference**, the engine estimates the conditional risk of icing and non-icing events linked to specific turbine control actions.
- This risk assessment framework supports *real-time* operational decision making.

## Results

- The transformer model exhibits **superior accuracy and F1-score** compared to both CNN and CNN-LSTM baselines.
- The Bayesian engine facilitates actionable recommendations by quantifying operational risk during both icing and non-icing periods.

## How to Use

1. **Clone the repository** and install dependencies as listed in `requirements.txt`.
2. **Prepare your data:** Ensure SCADA datasets are formatted as described above.
3. **Train Autoencoder:** Run the autoencoder for feature reduction.
4. **Train Detection Models:** Launch scripts for CNN, CNN-LSTM, and transformer-based models.
5. **Evaluate Results:** Compare performance metrics (accuracy, F1-score) among the models.
6. **Run Bayesian Engine:** Compute posterior probability risk based on detection output.

## Future Work

- Extend framework for adaptation to different geographical regions and turbine models.
- Integrate real-time deployment capabilities with cloud-based SCADA systems.
- Explore other advanced architectures and anomaly detection techniques.

