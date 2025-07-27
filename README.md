# Gradient-Aware Directional Convolution with Kolmogorov Arnold Network-Enhanced Feature Fusion for Road Extraction

## Abstract

Automatic road extraction from high-resolution remote sensing images is essential for urban and rural development, as well as traffic management and environmental preservation, enabling informed decisions for sustainable planning. In remote sensing images, roads are densely packed and occupy only a small portion of the image, surrounded by complex backgrounds. This makes it challenging to preserve the integrity and connectivity of the extracted road network. To address this problem, we propose GADC-KANNet, to enhance the detection and extraction of road pixels from remote sensing images. The proposed Gradient Aware Directional Convolution Layer (GADC) enhances the model’s ability to capture directional features, improving road pixel detection by adapting to the varying orientations of roads; the Dilated Residual Activation Path (DRAP) extends the receptive field by introducing dilated convolutions into the residual connections, allowing the model to capture more complex spatial and semantic patterns; and the Kolmogorov-Arnold Networks-based Feature Selection Fusion (KAN-FSF) module filters out redundant features and facilitates the seamless fusion of high-level and low-level information, optimizing the feature integration process for more accurate road extraction. Extensive experiments were conducted on the benchmark datasets MIT, DeepGlobe, and CHN6-CUG. These datasets feature varied road layouts, image resolutions, and environmental complexities. The results demonstrate that the proposed method outperforms the nearest competing approach, achieving a 1.86% improvement in precision on the MIT dataset, a 0.43% improvement in F1-score on the DeepGlobe dataset, and a 1.23% enhancement in F1-score on the CHN6-CUG dataset for road extraction tasks.

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



## Installation Guide (Using Conda)

```bash

# 1. Create the Conda environment
conda env create -f GADCKANNetenvironment.yml
conda activate road-extraction

# 2. Run .ipynb file
