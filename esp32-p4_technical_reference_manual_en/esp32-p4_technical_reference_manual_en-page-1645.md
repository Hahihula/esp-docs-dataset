

```markdown
Chapter 36 Image Signal Processor (ISP) GoBack


Figure 36.5-1. Gamma Curve

REG_GAMMA_Xn = log2(Xn·Xn−1)

REG_GAMMA_XF = log2(X0F-X0E+1)


36.5.2.9 RGB2YUV

The RGB2YUV module converts RGB888 pixels into full-range YUV422 format. The conversion protocol can be configured with ISP_YUV_MODE.


36.5.2.10 Sharpen

The sharpen module is used to sharpen images. This module separates the low-frequency and high-frequency components of the image using a low-pass filter template (such as a mean template or Gaussian template) via ISP_SHARP_FILTER_COE xx. For low-frequency components, no processing will be done. For high-frequency components, each pixel undergoes the following processing to achieve sharpening:

*   Pixels with frequencies below ISP_SHARP_THRESHOLD_LOW are set to 0.
*   Pixels with frequencies above ISP_SHARP_THRESHOLD_LOW but below ISP_SHARP_THRESHOLD_HIGH are multiplied by the coefficient ISP_SHARP_AMOUNT_LOW.
*   Pixels with frequencies above ISP_SHARP_THRESHOLD_HIGH are multiplied by the coefficient ISP_SHARP_AMOUNT_HIGH.

At the end of each frame, the maximum value of high-frequency component pixels in that frame can be obtained by reading ISP_SHARP_GRADIENT_MAX. This value can serve as a reference for configuring settings for the next frame.


36.5.2.11 Contrast/Hue/Saturation/Luminance Adjustment (COLOR)

This module is designed to modify the contrast, saturation, hue, and luminance of an image. Contrast, saturation, and luminance are configured through ISP_COLOR_CONTRAST, ISP_COLOR_SATURATION, and ISP_COLOR_BRIGHTNESS, respectively. Hue adjustment is achieved by combining ISP_COLOR_HUE_H and ISP_COLOR_HUE to form a 9-bit control value.
```