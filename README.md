# Gradient-Aware Directional Convolution with Kolmogorov Arnold Network-Enhanced Feature Fusion for Road Extraction

## Abstract

Automatic road extraction from high-resolution remote sensing images is essential for urban and rural development, as well as traffic management and environmental preservation, enabling informed decisions for sustainable planning. In remote sensing images, roads are densely packed and occupy only a small portion of the image, surrounded by complex backgrounds. This makes it challenging to preserve the integrity and connectivity of the extracted road network. To address this problem, we propose GADC-KANNet, to enhance the detection and extraction of road pixels from remote sensing images. The proposed Gradient Aware Directional Convolution Layer (GADC) enhances the model’s ability to capture directional features, improving road pixel detection by adapting to the varying orientations of roads; the Dilated Residual Activation Path (DRAP) extends the receptive field by introducing dilated convolutions into the residual connections, allowing the model to capture more complex spatial and semantic patterns; and the Kolmogorov-Arnold Networks-based Feature Selection Fusion (KAN-FSF) module filters out redundant features and facilitates the seamless fusion of high-level and low-level information, optimizing the feature integration process for more accurate road extraction. Extensive experiments were conducted on the benchmark datasets MIT, DeepGlobe, and CHN6-CUG. These datasets feature varied road layouts, image resolutions, and environmental complexities. The results demonstrate that the proposed method outperforms the nearest competing approach, achieving a 1.86% improvement in precision on the MIT dataset, a 0.43% improvement in F1-score on the DeepGlobe dataset, and a 1.23% enhancement in F1-score on the CHN6-CUG dataset for road extraction tasks.

---

## Architecture Overview
The proposed GADC-KANNet architecture consists of the following key components:

- **Gradient-Aware Directional Convolution Layer (GADC)** 

-- Captures orientation-sensitive features

-- Enhances road pixel detection by adapting to varying road directions

- **Dilated Residual Activation Path (DRAP)**

Incorporates dilated convolutions within residual blocks

Expands the receptive field to capture complex spatial and semantic patterns

- **Kolmogorov-Arnold Networks-Based Feature Selection Fusion (KAN-FSF)**

Filters redundant features

Enables effective fusion of high-level and low-level features for accurate road extraction

- **Encoder-Decoder Backbone**

Extracts multi-scale features from remote sensing images

Produces segmentation masks through upsampling and skip connections

- **End-to-End Training Pipeline**

Trains on high-resolution satellite images

Optimized with supervised loss functions for binary segmentation

The architecture comprises the following core components:

- **Backbone Encoder**: A lightweight or ResNet-based encoder to extract hierarchical feature maps.
- **Gradient-Aware Directional Convolution (GADC)**: A custom convolutional module that incorporates directional gradient cues to strengthen feature maps near road boundaries.
- **KAN-Enhanced Feature Fusion**: Inspired by the Kolmogorov–Arnold theorem, this module fuses multi-scale features using learnable nonlinear mappings, outperforming traditional additive or concatenation-based fusion.
- **Decoder**: Upsampling layers with skip connections for pixel-wise prediction of road masks.

> 📌 *Add your architecture diagram below by replacing the placeholder image link.*

![Architecture Overview](https://your-domain.com/architecture-diagram.png)

---

## ✨ Key Features

- ✅ **Directional Awareness** via GADC: Captures orientation-sensitive road structures.
- ✅ **Nonlinear Feature Fusion**: KAN fusion generalizes better with fewer parameters.
- ✅ **Plug-and-Play Design**: Compatible with most encoder-decoder segmentation backbones.
- ✅ **End-to-End Training**: No need for post-processing like CRFs.
- ✅ **Scalable**: Easily adaptable to different satellite imagery datasets.

---

## ⚙ Installation Guide (Using Conda)

```bash
# 1. Clone the repository
git clone https://github.com/your-username/Gradient-Aware-Road-Extraction.git
cd Gradient-Aware-Road-Extraction

# 2. Create the Conda environment
conda env create -f environment.yml
conda activate road-extraction

# 3. (Optional) Install in editable mode
pip install -e .

