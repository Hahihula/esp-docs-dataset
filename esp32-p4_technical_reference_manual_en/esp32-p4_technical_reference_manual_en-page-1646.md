

```markdown
## Chapter 36 Image Signal Processor (ISP)

### 36.5.2.12 YUV_Limit and YUV2RGB

The YUV_Limit module converts full-range YUV422 pixels to limited-range YUV422 pixels. This module is activated only when RGB2YUV is enabled, YUV2RGB is disabled, and `ISP_YUV_RANGE` is set to 1. With this configuration, the ISP output type is either YUV422 or YUV420.

YUV2RGB converts full-range YUV422 pixels to RGB888 format. The conversion protocol can be configured with `ISP_YUV_MODE`.

**Note:**
For full-range YUV, Y, U, and V channels range from 0 to 255.
For limited-range YUV, Y channel ranges from 16 to 235, and U and V channels range from 16 to 240.

### 36.5.2.13 Cropping (CROP)

The CROP module performs image cropping. The start and end coordinates in the X and Y directions are configured using `ISP_CROP_X_START`, `ISP_CROP_X_END`, `ISP_CROP_Y_START`, and `ISP_CROP_Y_END`, respectively. The start coordinates must be even, and the end coordinates must be odd.

### 36.5.2.14 Automatic Exposure Statistics (AE)

Auto Exposure (AE) uses 25 statistical sub-windows for image luminance statistics, forming a 5 x 5 grid of statistical window. The size of these windows is set using the register `ISP_AE_BX/BY_REG`. Each sub-window is numbered as shown in Figure 36.5-2. The average luminance of each sub-window, represented as an 8-bit value, can be read with `ISP_AE_Bxx_MEAN`. These statistics can be utilized to implement automatic exposure algorithms for cameras.

![Figure 36.5-2. Sub-Window Numbering](image-placeholder)

AE utilizes two data sampling points: the output of the Demosaic module and the output of the Gamma module. These sampling points can be configured using `ISP_AE_SELECT`.

AE also includes a simple luminance monitoring module, implemented either by hardware or software. This module calculates the average luminance of all sub-windows every `ISP_AE_MONITOR_PERIOD` frames. If the average luminance falls outside the thresholds set by `ISP_AE_MONITOR_TH/TL`, interrupt for AE luminance
```