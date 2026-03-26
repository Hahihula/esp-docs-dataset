

```markdown
- When MIPI-CSI is the input, set the input type via `ISP_DATA_TYPE`
- When DVP is the input, set `ISP_DATA_TYPE` to 0, then set the data type via `ISP_CAM_DATA_TYPE`
- When VDMA is the input, set the input type via `ISP_DATA_TYPE`, and configure
  `ISP_DMA_DATA_TYPE` accordingly

## 36.5.2 ISP_Pipeline

ISP_Pipeline is the core of ISP, housing all the image processing algorithms. Each algorithm module can be enabled or disabled via the corresponding bit of `ISP_CNTL_REG`. Except for modules related to color space conversion (demosaic, RGB2YUV, and YUV2RGB), other modules can be enabled or disabled dynamically without the need to shut down the ISP for reconfiguration. Moreover, once enabled, each algorithm module generates an end-of-frame interrupt, capable of triggering an interrupt after processing each image frame.

### 36.5.2.1 Black Level Correction (BLC)

This module is used to subtract the black level offset of the sensor. The black level offset to be subtracted for each Bayer channel is configured via `ISP_BLC_Rx_VALUE`. With the black level offset subtracted, the pixel range will be reduced, which can be stretched back to 0-255 via `ISP_BLC_Rx_STRETCH`.

There are four Bayer channels in total. The mapping between channel and index is as follows:

* RO refers to the top-left channel
* R1 refers to the top-right channel
* R2 refers to the bottom-left channel
* R3 refers to the bottom-right channel

### 36.5.2.2 Defective Pixel Correction (DPC)

This module removes defective pixels from the input image. DPC supports both dynamic correction and static correction, which are controlled by `ISP_STA_EN` and `ISP_DYN_EN`, respectively. The two correction modes can be enabled simultaneously.

Dynamic correction automatically detects defective pixels based on the input pixel values and replaces them with the median value. Two defective pixel detection algorithms are supported:

* **Algorithm 0**: Compute the minimum value `min8` and the maximum value `max8` among the eight neighboring pixels of the current pixel. If the current pixel value is greater than `max8 + ISP_DPC_THRESHOLD_H`, or less than `min8 - ISP_DPC_THRESHOLD_L`, the pixel is classified as defective.

* **Algorithm 1**: Let the current pixel value be `pix`. Compute the mean value `est` of the eight neighboring pixels, and the absolute difference `dif = |est - pix|`. Define `avg = (sum of the eight neighbors + 8 × pix) / 16`. Detection is performed in two steps:

    * **Step 1**: Determine the maximum value `max8` among the eight neighboring pixels. If `pix < max8 × ISP_DPC_THRESHOLD_H` and `pix > max8 × ISP_DPC_THRESHOLD_L`, the pixel is considered non-defective; otherwise, proceed to Step 2.
    * **Step 2**: The pixel is classified as defective if either of the following conditions is met:
```