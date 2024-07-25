# Image Denoising using Soft-Thresholding

This project implements the denoising method using soft-thresholding as described in the seminal paper [Denoising by Soft-Thresholding](https://statweb.stanford.edu/~donoho/Reports/1995/denoisereport.pdf) by David L. Donoho. The method leverages wavelet transforms and soft-thresholding to effectively remove noise from signals while preserving important features such as edges.

## Overview

Denoising by soft-thresholding is a powerful technique for removing noise from signals and images. Traditional denoising methods often struggle to preserve critical features like edges, whereas soft-thresholding provides a balance between noise reduction and feature preservation.

## Implementation

The implementation involves the following steps:
1. **Wavelet Transform**: Decompose the noisy signal into wavelet coefficients at various scales.
2. **Thresholding**: Apply a universal threshold to the wavelet coefficients. The threshold is determined based on the noise level.
3. **Soft-Thresholding**: Apply the soft-thresholding rule to shrink the wavelet coefficients.
4. **Inverse Wavelet Transform**: Reconstruct the denoised signal from the thresholded wavelet coefficients.

### Soft-Thresholding Rule

For each wavelet coefficient \( w \), the soft-thresholding rule is:
\[ w' = \text{sign}(w) \cdot \max(|w| - \lambda, 0) \]
where \( \lambda \) is the threshold value.

### Universal Threshold

The universal threshold \( \lambda \) is given by:
\[ \lambda = \sigma \sqrt{2 \log n} \]
where \( \sigma \) is the estimated noise level and \( n \) is the number of data points.

## Usage

### Dependencies

The following Python libraries are required:
- numpy
- pywt
- matplotlib

Install the required libraries using pip:
```sh
pip install numpy pywt matplotlib
