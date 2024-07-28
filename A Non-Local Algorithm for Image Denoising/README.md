# Non-Local Means Denoising Algorithm

## Overview

The Non-Local Means (NL-Means) algorithm is a powerful method for image denoising that leverages the redundancy in natural images. Unlike traditional denoising techniques that rely on local information, NL-Means uses non-local information by comparing patches from different parts of the image. This approach helps in preserving important details such as edges and textures while effectively reducing noise.

## Key Concepts

### Patch-Based Denoising
Instead of denoising each pixel independently, NL-Means denoises small patches of the image. A patch is a small, square block of pixels centered around a specific pixel.

### Similarity Measure
The similarity between patches is measured using a weighted Euclidean distance. Patches that are more similar to the central patch will have higher weights in the averaging process.

## Algorithm Steps

1. **Define Patches and Search Window**
   - A patch is a small, square block of pixels centered around a specific pixel.
   - A search window around the central pixel defines the area where the algorithm looks for similar patches.

2. **Compute Patch Similarity**
   - The similarity between two patches is computed using a Gaussian weighted Euclidean distance.

3. **Compute Weights**
   - The weight for each patch within the search window is computed using an exponential function based on the similarity measure.

4. **Denoise the Pixel**
   - The denoised value of the central pixel is obtained by computing the weighted average of all pixels in the search window.
