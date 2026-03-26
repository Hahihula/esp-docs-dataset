

```markdown
36.5.2.15 Automatic Focus Statistics (AF)

AF gathers luminance and sharpness information within specified statistical windows based on the output of the sharpen module. There are 3 independent statistical windows, and the size and position of each window can be configured using ISP_AF_H/VSCALE_A/B/C_REG. The module supports automatic and manual trigger modes for statistics collection. The results of luminance and sharpness statistics for each window can be accessed using ISP_AF_LUMA/B/C and ISP_AF_SUMA/B/C. These statistics can be used to implement automatic focus algorithms for cameras.

AF also includes a focus scene monitoring module, which users can choose to implement hardware-based monitoring with this module or implement via software. This module evaluates cumulative changes in luminance and sharpness across all statistical windows as criteria. It performs statistics every ISP_AF_ENV_PERIOD frames. If consecutive statistics show a difference from baseline values for luminance and sharpness that exceeds the specified threshold, an interrupt is triggered indicating a change in the focus scene that requires refocusing. The baseline values are automatically updated after each automatic or manually triggered statistics collection. There are three methods for setting the threshold:

* Directly set the luminance and sharpness thresholds using ISP_AF_ENV_USER_THRESHOLD_LUM and ISP_AF_ENV_USER_THRESHOLD_SUM
* If ISP_AF_ENV_USER_THRESHOLD_SUM is 0, use the corresponding baseline sharpness value multiplied by ISP_AF_ENV_THRESHOLD (4 fractional bits) as the sharpness threshold
* If ISP_AF_ENV_USER_THRESHOLD_LUM is 0, use the corresponding baseline luminance value multiplied by ISP_AF_ENV_THRESHOLD (4 fractional bits) as the luminance threshold

36.5.2.16 Automatic White Balance Statistics (AWB)

AWB gathers white balance information for specified windows containing white patches. The coordinates of the window can be set using ISP_AWB_H/VSCALE_REG. White patches are filtered based on luminance limits ISP_AWB_MAX/MIN_LUM, R/G limits ISP_AWB_MAX/MIN_RG, and B/G limits ISP_AWB_MAX/MIN_BG.

The statistics include the number of white patches and the accumulated values of the R, G, B components for all white patches. These statistics can be obtained using ISP_AWBO_WHITE_CNT and ISP_AWBO_ACC_R/G/B. They can be used to implement automatic white balance algorithms in cameras.

In addition, AWB supports dividing the window into 5 × 5 sub-windows, which are configured via ISP_AWB_X_START, ISP_AWB_X_BSIZE, ISP_AWB_Y_START, and ISP_AWB_Y_BSIZE. The sub-window range must not exceed the range of the main window. The statistics results are written to the AWB LUT and can be accessed by setting ISP_LUT_NUM = 2. The detailed access procedure can be found in Section 36.5.2.4. The statistics are stored in the order of sub-windows from left to right and from top to bottom. Each sub-window occupies four consecutive addresses, which store, from low to high addresses, the number of white patches, and the accumulated values of the R, G, B components for white patches.
```