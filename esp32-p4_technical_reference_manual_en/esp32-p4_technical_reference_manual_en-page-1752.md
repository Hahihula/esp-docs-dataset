

# Chapter 37
## Pixel-Processing Accelerator (PPA)

### 37.1 Overview

ESP32-P4 includes a pixel-processing accelerator (PPA) designed for 2D image display. This module realizes hardware-level acceleration of image algorithms and implements functions such as image rotation, scaling, mirroring, and blending.

PPA consists of two functional modules: scaling-rotation-mirroring (SRM) and image blending (BLEND). The SRM module implements image rotation, scaling, and XY-axis mirroring functions, while the BLEND module achieves the blending of two layers of the same size based on the Alpha channel, i.e., transparency.

PPA processes images in units of pixel block. These pixel blocks are acquired from memory through 2D-DMA. The connection between PPA and 2D-DMA is shown in Figure 371-1.

![Figure 371-1. PPA 2D-DMA Connection](image_not_rendered_here)

### 37.2 Terminology

To better illustrate the functions of the PPA module, the following terms are used in this chapter:

*   **image**: A complete image stored in the system memory
*   **image block**: A portion cropped from an image at a certain size, with the maximum size equivalent to the entire image. i.e., hb, vb size under 2D-DMA 2D-MODO.
*   **pixel block**: A portion cropped from an image block. SRM reads and writes data in pixel blocks.

### 37.3 Features

• Image rotation, scaling, and mirroring by SRM: