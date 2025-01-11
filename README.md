# 3D Reconstruction

This project demonstrates a complete pipeline on how to reconstruct a 3D model from a single 2D image using deep learning. It leverages a pre-trained depth estimation model from Hugging Face and the Open3D library for 3D processing, the script takes a 2D image as input, estimates its depth map, generates a 3D point cloud, and finally reconstructs a 3D mesh. The output consists of a `.ply` point cloud file and an `.obj` mesh file, which can be viewed in standard 3D modeling software. This project provides a complete pipeline for converting 2D images into basic 3D representations.


https://github.com/user-attachments/assets/3e0851f8-6e8d-468e-87bd-40f9fbf5996b

*3D Reconstruction - 2D Image (Left), 3D Point-Cloud (Below), 3D Mesh (Top)*


## Overview

The process involves the following steps:

1.  **Depth Estimation:** A pre-trained depth estimation model (Intel/dpt-hybrid-midas) predicts a depth map from the input image.
2.  **Point Cloud Generation:** The depth map is converted into a 3D point cloud using camera intrinsics.
3.  **Point Cloud Post-processing:** Outlier removal and normal estimation are performed to refine the point cloud.
4.  **Mesh Reconstruction:** Poisson surface reconstruction is used to create a 3D mesh from the point cloud.

## Requirements

*   Python 3
*   PyTorch
*   Torchvision
*   Torchaudio
*   Pillow (PIL)
*   Transformers
*   Open3D
*   Matplotlib

You can install the required packages using the following command:

```
pip install torch torchvision torchaudio Pillow transformers open3d matplotlib
```

## Usage 

1. **Clone the repository:**
```
git clone <repository_url>

```

2. 
