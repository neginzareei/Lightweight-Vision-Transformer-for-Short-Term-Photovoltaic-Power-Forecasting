# Lightweight-Vision-Transformer-for-Short-Term-Photovoltaic-Power-Forecasting

## Overview

This repository presents the research project associated with our manuscript currently under review.

The study investigates short-term photovoltaic (PV) power forecasting using ground-based sky images and a lightweight Vision Transformer architecture. The proposed framework combines MobileViT-XXS for spatial feature extraction with a Gated Recurrent Unit (GRU) for temporal modeling, enabling accurate solar power forecasting with significantly lower computational requirements than conventional Transformer-based approaches.

## Research Motivation

Accurate short-term forecasting of photovoltaic power generation is essential for:

* Distribution network operation
* Voltage regulation
* Renewable energy integration
* Grid stability
* Reserve scheduling

While Vision Transformers have shown strong performance in image-based forecasting tasks, many existing models rely on computationally expensive architectures that are difficult to deploy in real-time or resource-constrained environments.

This work investigates whether a lightweight Vision Transformer can achieve competitive forecasting performance while maintaining low computational complexity.

## Dataset

Stanford SKIPP'D Dataset

* Years: 2017–2019
* Sky images: 64×64 pixels
* Temporal resolution: 1 minute
* PV plant capacity: 30.1 kW
* Location: Stanford University, California

Input:

* Six consecutive sky images

Output:

* PV power prediction 15 minutes ahead

## Proposed Architecture

Sky Images (64×64)
↓
MobileViT-XXS
(Spatial Feature Extraction)
↓
320-D Feature Vectors
↓
Bidirectional GRU
(Temporal Modeling)
↓
Regression Head
↓
15-Minute Ahead PV Power Forecast

Key Components:

* MobileViT-XXS (~1.3M parameters)
* Bidirectional GRU
* AdamW optimization
* Mixed precision training
* Early stopping

## Main Results

| Model                | RMSE (kW) | MAE (kW) | nRMSE (%) |
| -------------------- | --------- | -------- | --------- |
| Persistence Baseline | 3.661     | 2.015    | 12.42     |
| Proposed Model       | 2.598     | 1.380    | 8.78      |

### Improvement

* 29% relative reduction in forecasting error
* Significant improvement over persistence forecasting
* Competitive accuracy with substantially fewer parameters than conventional Vision Transformer approaches

## Contributions

* Developed a lightweight Vision Transformer framework for image-based PV forecasting.
* Combined MobileViT-XXS and GRU for efficient spatio-temporal learning.
* Demonstrated accurate forecasting using only low-resolution sky images.
* Achieved strong performance with approximately 1.3 million parameters.
* Improved suitability for edge deployment and real-time operation.


## Keywords

Vision Transformer • MobileViT • Renewable Energy • Solar Forecasting • Deep Learning • Computer Vision • Time-Series Forecasting • Edge AI • Smart Grids

## Publication Status

The associated manuscript is currently under peer review.

To preserve the integrity of the review process, the implementation code remains private and will be released after publication.

Researchers and potential collaborators are welcome to contact the authors for additional information.
