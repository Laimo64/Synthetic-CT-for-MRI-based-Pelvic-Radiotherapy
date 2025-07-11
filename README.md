# Synthetic-CT-for-MRI-based-Pelvic-Radiotherapy
This repository contains the implementation and evaluation of three deep learning models for generating synthetic CT (sCT) from MRI scans, designed to assist radiotherapy planning while reducing patient radiation exposure.

## Project Overview
Modern radiotherapy heavily relies on CT images for dose planning and anatomical localization. However, CT involves ionizing radiation. To eliminate this exposure while preserving critical imaging information, we propose a MRI-only workflow by generating synthetic CT images (sCT) using deep learning.
This project compares three model architectures for MR-to-CT synthesis:
-  Pix2Pix (GAN-based)
-  MSEP (U-Net + Swin Transformer hybrid)

## Methodology
1. Pix2Pix (cGAN)
   - Image-to-image translation using conditional GAN with LSGAN loss.
   - L1 loss (MAE) encourages pixel-level similarity and reduces image blur.
   - Best overall performance in SSIM and PSNR.
2. MSEP (Multi-scale Structure Extraction and Preservation.)
   - Combines 3D U-Net with Swin Transformer blocks in skip connections.

### References
This work is based on open-source models and the SynthRAD2023 dataset. 
