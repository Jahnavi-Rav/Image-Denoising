# Image Denoising using Anisotropic Diffusion

This project implements the anisotropic diffusion algorithm for image denoising, as described in the seminal paper [Scale-Space and Edge Detection Using Anisotropic Diffusion](https://ieeexplore.ieee.org/document/572797) by Pietro Perona and Jitendra Malik.

## Overview

Anisotropic diffusion is a technique for edge-preserving image smoothing. Traditional image smoothing techniques like Gaussian filtering tend to blur edges, which are crucial features in an image. Anisotropic diffusion aims to overcome this by diffusing the image in a way that respects edges.

## Implementation

The implementation of the anisotropic diffusion algorithm can be found in the `Denoising/subfolder1/Scale_space_and_edge_detection_using_Anisotropic_diffusion.ipynb` file.

## How to Use

1. **Place an image file in the project directory.**
2. **Update the image path in `Denoising/subfolder1/Scale_space_and_edge_detection_using_Anisotropic_diffusion.ipynb`.**
3. **Run the notebook to see the original and denoised images.**

### Parameters

- `num_iter`: Number of iterations for the diffusion process.
- `K`: Conductivity parameter controlling the sensitivity to edges.
- `delta_t`: Time step for the diffusion process.

### Requirements

- numpy
- matplotlib
- scipy
- scikit-image

Install the requirements using pip:

```sh
pip install numpy matplotlib scipy scikit-image
