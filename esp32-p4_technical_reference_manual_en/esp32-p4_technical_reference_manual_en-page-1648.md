

```markdown
36.5.2.17 Histogram Statistics (HIST)

HIST calculates brightness information for the image through statistical analysis. This module can define a statistical window, which can be divided into 5 x 5 sub-windows similar to AE. The configuration is done using registers ISP_HIST_OFFS_REG and ISP_HIST_SIZE_REG. The weight of each sub-window can be independently adjusted with ISP_HIST_WEIGHT_xx.

The statistics are presented as a histogram with 16 intervals. The x-axis of the histogram is defined using ISP_HIST_SEG_x_x, and the final statistics can be retrieved using ISP_HIST_BIN_x.

HIST involves three data sampling points: BF, demosaic, and RGB2YUV, corresponding to RAW, RGB, and YUV data sampling points respectively. These can be configured using ISP_HIST_MODE. When the sampling point is set to RGB, RGB weighting coefficients can be adjusted via ISP_HIST_COEFF_R/G/B.

36.5.3 ISP_Tail

ISP_Tail is the post-processing section that handles data from two input sources, ultimately outputting in Image Interface 64 format to CSI_Bridge.

When the ISP is turned off, ISP_Tail receives Image Interface 32 data from the MIPI CSI HOST, converts it to Image Interface 64 format, and outputs it to CSI_Bridge. The byte order of the input Image Interface 32 data can be adjusted using ISP_BYTE_ENDIAN_ORDER.

When the ISP is turned on, ISP_Tail receives data from ISP_Pipeline and processes them before outputting to CSI_Bridge. This processing includes:

*   Converting RGB888 to RGB565 based on register configurations
*   Converting YUV422 to YUV420 based on register configurations
*   Converting data from ISP_Pipeline to Image Interface 64 format

36.5.4 Sequence Control

For modules involving matrix operations, it is necessary to buffer multiple lines of data before starting operations. In such cases, it is crucial for the module to generate an output sequence when the last few lines of image data are buffered. This output sequence can be controlled using ISP_BF/DEMOSAIC/SHARP_TAIL_PIXEN_PULSE_TH/TL, to prevent buffer overflow in the CSI_Bridge due to excessive speed. Please exercise caution when setting this register too large, as it may disrupt the normal data sequence. TH must be smaller than ISP_HADR_NUM-1, and it is recommended to set ISP_BF/DEMOSAIC/SHARP_TAIL_PIXEN_PULSE_TH/TL to a value less than or equal to 8.

36.5.5 Shadow Registers

Some ISP modules support shadow registers. The supported modules include:

*   BLC
*   DPC
```