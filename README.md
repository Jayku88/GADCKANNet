# will be updated after publication (to avoid similarity)

## Abstract
will be updated after publication (to avoid similarity)

---

## Architecture Overview
The proposed GADC-KANNet architecture consists of the following key components:

- **Gradient-Aware Directional Convolution Layer (GADC)**: Captures orientation-sensitive features, Enhances road pixel detection by adapting to varying road directions

- **Dilated Residual Activation Path (DRAP)**: Incorporates dilated convolutions within residual blocks, Expands the receptive field to capture complex spatial and semantic patterns

- **Kolmogorov-Arnold Networks-Based Feature Selection Fusion (KAN-FSF)**: Filters redundant features, Enables effective fusion of high-level and low-level features for accurate road extraction

- **Encoder-Decoder Backbone**: Extracts multi-scale features from remote sensing images, Produces segmentation masks through upsampling and skip connections

- **End-to-End Training Pipeline**: Trains on high-resolution satellite images, Optimized with supervised loss functions for binary segmentation

---
## System Configuration

All experiments and model training were conducted on a high-performance computing setup with the following specifications:

- **Operating System**: Ubuntu 20.04.6 LTS (Focal)
- **CPU**: AMD Ryzen 9 7950X (16 Cores, 32 Threads)
  - Base Clock: 3.0 GHz  
  - Boost Clock: Up to 5.88 GHz  
  - L3 Cache: 64 MB
- **RAM**: 128 GB DDR4
- **GPU**: NVIDIA RTX A6000
  - Memory: 48 GB GDDR6  
  - CUDA Version: 12.5  
  - Driver Version: 555.42.02
---
## Dataset Details

This project utilizes three benchmark datasets for road extraction from remote sensing imagery:

### 1. Massachusetts Roads Dataset (MIT)

- **Format**:
  - RGB images (`.tiff`)
  - Binary road masks (1 = road, 0 = background, `.tif`)
- **Resolution**: 1500 × 1500 pixels
- **Source**: [MIT](https://www.cs.toronto.edu/~vmnih/data/)

### 2. DeepGlobe Road Extraction Dataset (DG)

- **Format**:
  - RGB images (`.jpg`)
  - Binary road masks (1 = road, 0 = background, `.png`)
- **Resolution**: 1024 × 1024 pixels
- **Source**: [DG](https://ieeexplore.ieee.org/document/8575485)

### 3. CHN6-CUG Road Dataset (CC)

- **Format**:
  - RGB images (`.jpg`)
  - Binary road masks (1 = road, 0 = background, `.png`)
- **Resolution**: 512 × 512 pixels
- **Source**: [CC](https://www.sciencedirect.com/science/article/pii/S0924271621000873)

---
## Installation Guide (Using Conda)

```bash

# 1. Create the Conda environment
conda env create -f GADCKANNetenvironment.yml
conda activate tfclone

# 2. Run GADCKANNet-MIT.ipynb file using environment tfclone
