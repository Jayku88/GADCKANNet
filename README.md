# GADCKANNet

Kolmogorov Arnold Network-Enhanced Feature Fusion for Road Extraction
🧠 Project Title and Abstract
Title: Gradient-Aware Directional Convolution with Kolmogorov Arnold Network-Enhanced Feature Fusion for Road Extraction

Abstract:
Accurate road extraction from satellite imagery is a critical task for geospatial analysis, urban planning, and autonomous navigation. This work proposes a novel deep learning framework combining Gradient-Aware Directional Convolution (GADC) with Kolmogorov–Arnold Network (KAN)-based feature fusion. GADC leverages spatial gradient orientations to enhance edge-aware representations, while the KAN module enables complex nonlinear feature interactions with high generalization capacity. Experimental results on standard remote sensing datasets demonstrate significant improvements in road segmentation accuracy, continuity, and robustness to occlusions compared to conventional CNN and transformer-based methods.

🏗 Architecture Overview
The architecture comprises the following core components:

Backbone Encoder: A lightweight or ResNet-based encoder to extract hierarchical feature maps.

Gradient-Aware Directional Convolution (GADC): A custom convolutional module that incorporates directional gradient cues to strengthen feature maps near road boundaries.

KAN-Enhanced Feature Fusion: Inspired by the Kolmogorov–Arnold theorem, this module fuses multi-scale features using learnable nonlinear mappings, outperforming traditional additive or concatenation-based fusion.

Decoder: Upsampling layers with skip connections for pixel-wise prediction of road masks.

<p align="center"> <img src="https://your-domain.com/architecture-diagram.png" alt="Architecture Overview" width="700"/> </p>
