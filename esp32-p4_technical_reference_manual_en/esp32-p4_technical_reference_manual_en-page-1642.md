

```markdown
Chapter 36 Image Signal Processor (ISP)

* dif > avg× ISP_DPC_FACTOR_DARK and est ≥ pix
* dif > (255 − avg) × ISP_DPC_FACTOR_BRIG and est < pix

Static correction is implemented using a defective pixel coordinate lookup table (LUT). Pixels whose coordinates are stored in the LUT are replaced with the median value. The defective pixel coordinates must be obtained through static calibration. During calibration, neither static nor dynamic correction can be enabled.

The calibration procedure is as follows:

- Black image defective pixel calibration
  - Set ISP_DPC_BLACK_EN = 1
  - Set ISP_DPC_CHECK_EN = 1
  - Set ISP_DPC_EN = 1
    - Input a black image and wait for the calibration to complete
  - Set ISP_DPC_CHECK_EN = 0
  - Software reads all defective pixel coordinates for the black image from the LUT registers

- White image defective pixel calibration
  - Set ISP_DPC_BLACK_EN = 0
  - Set ISP_DPC_CHECK_EN = 1
  - Set ISP_DPC_EN = 1
    - Input a white image and wait for the calibration to complete
  - Set ISP_DPC_CHECK_EN = 0
  - Software reads all defective pixel coordinates for the white image from the LUT registers

- Software merges the defective pixel coordinates obtained from the black and white images, removes duplicates, and writes the final list back to the LUT

The LUT read and write procedure is described in Section 36.5.2.4. By setting ISP_LUT_NUM = 1, the defective pixel coordinate LUT for DPC is selected. This LUT has a depth of 512, allowing up to 512 defective pixel coordinates to be stored.

36.5.2.3 Bayer Filter (BF)

This module is designed for denoising input images in the Bayer domain. The denoising strength can be adjusted using ISP_SIGMA, and the denoising template can be fine-tuned using ISP_GAU_TEMPLATExx.

36.5.2.4 Lens Shading Correction (LSC)

This module is utilized for lens shading correction in the Bayer domain. It corrects the R, Gr, Gb, and B channels independently by dividing each channel into a 32 x 32 grid (equivalent to a 64 x 64 division for the entire image) and stores the correction coefficients for each channel in a lookup table (LUT).

Before using this module, calibration is necessary to obtain the LUT correction coefficients. Specifically, first we capture a white image in a scene with uniform ambient lighting. Divide the image into a 32 x 32 grid for
```