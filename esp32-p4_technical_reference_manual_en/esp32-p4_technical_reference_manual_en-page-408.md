

```markdown
Figure 6.4-5. Color Space Conversion

Color space conversion is performed in 3 stages. The first stage converts a specific 16-bit color format (2 bytes/pixel) to a 24-bit color format (3 bytes/pixel). The source color formats can be configured via the DMA2D_OUT_COLOR_INPUT_SEL_CHn or DMA2D_IN_COLOR_INPUT_SEL_CH0 field. (See the supported color format conversion in the first stage by clicking the fields)

The second stage further converts the output data of the first stage using the following formula:

    256 * Q = A[9:0] * x + B[10:0] * y + C[9:0] * z + D[17:0]

In this formula, Q is the output data; x, y, and z are the most significant, middle, and the least significant byte of the input data respectively; A, B, C, and D are the corresponding multiplication or addition coefficients, which are signed numbers. At most 3 bytes of data can be processed in one go, and therefore 3 * 4 = 12 coefficients need to be configured via the following fields:

*   DMA2D_OUT_COLOR_PARAM_H0_CHn/DMA2D_IN_COLOR_PARAM_H0_CHO
*   DMA2D_OUT_COLOR_PARAM_H1_CHn/DMA2D_IN_COLOR_PARAM_H1_CHO
*   DMA2D_OUT_COLOR_PARAM_MO_CHn/DMA2D_IN_COLOR_PARAM_MO_CHO
*   DMA2D_OUT_COLOR_PARAM_M1_CHn/DMA2D_IN_COLOR_PARAM_M1_CHO
*   DMA2D_OUT_COLOR_PARAM_LO_CHn/DMA2D_IN_COLOR_PARAM_LO_CHO
*   DMA2D_OUT_COLOR_PARAM_L1_CHn/DMA2D_IN_COLOR_PARAM_L1_CHO

PARAM_Hx, PARAM_Mx, and PARAM_Lx (x is 0 or 1) in field names represent the parameters for the three bytes of data respectively. Take PARAM_Hx as examples, the lower 10 bits of the 21-bit PARAM_H0 is coefficient A, the higher 11 bits of PARAM_H0 is coefficient B, the lower 10 bits of the 28-bit PARAM_H1 is coefficient C, and the higher 18 bits of PARAM_H1 is coefficient D.

The third stage, similar to the first stage, outputs the color format converted in the second stage directly, or further converts the 24-bit color format (3 bytes/pixel) to a 16-bit color format. This is configured using DMA2D_OUT_COLOR_OUTPUT_SEL_CHn or DMA2D_IN_COLOR_OUTPUT_SEL_CHO.

The following table lists the parameter configurations for commonly used color space conversions:

Table 6.4-6. Parameter Configuration for Color Space Conversion in TX Direction

| Conversion         | input_sel | proc_en | output_sel | param_h0   | param_h1   | param_m0   | param_m1   | param_l0   | param_l1   |
|--------------------|-----------|---------|------------|------------|------------|------------|------------|------------|------------|
| No conversion      | 7         | N/A     | N/A        | N/A        | N/A        | N/A        | N/A        | N/A        | N/A        |
| Only scramble order| 2/3       | 0       | 2          | N/A        | N/A        | N/A        | N/A        | N/A        | N/A        |

Cont'd on next page
```