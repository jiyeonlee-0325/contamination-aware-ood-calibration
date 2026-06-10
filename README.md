# Contamination-Aware Adaptive Calibration for Post-hoc OOD Detection

This repository contains the code for our project on contamination-aware adaptive calibration for post-hoc out-of-distribution detection.

## Project Overview

Post-hoc OOD detectors often assume that the calibration set used for threshold selection is clean. However, in realistic deployment settings, calibration data may contain hidden OOD samples.

This project studies how calibration-set contamination affects post-hoc OOD detection and evaluates robust calibration strategies.

## Experimental Setup

- ID dataset: CIFAR-10
- OOD dataset: SVHN
- Backbone classifier: ResNet-18 adapted for CIFAR-10
- OOD detectors: MSP, Energy, KNN, ViM, ODIN
- Contamination ratios: 0%, 1%, 5%, 10%, 20%
- Metrics: FPR95, ID TPR

## Environment Setup

Install the required packages with:

```bash
pip install -r requirements.txt

## Data

CIFAR-10 and SVHN are public datasets and are downloaded automatically using `torchvision.datasets`.

No private data or private credentials are required.

## How to Reproduce

The main notebook is:

```text
OOD_Detection.ipynb


### 3. Main Results 섹션
```markdown
## Main Results

The main results include:

- FPR95 degradation under contaminated calibration
- FPR95 reduction with fixed lower-tail trimming
- ID TPR trade-off analysis
- Adaptive calibration results using IQR and GMM
