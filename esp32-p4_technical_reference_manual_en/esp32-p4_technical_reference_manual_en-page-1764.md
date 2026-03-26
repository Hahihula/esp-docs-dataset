

```markdown
| Error Type                     | Details                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| PPA_RX_DSCR_HB_ERR_ST           | The sum of the horizontal size HB of the input image block configured in the SRM input descriptor and the horizontal offset X exceeds the entire image’s horizontal size HA configured in the output descriptor |
| PPA_XDST_LEN_TOO_SAMLL_ERR_ST   | The horizontal size of the image block after SRM scaling is 0             |
| PPA_XDST_LEN_TOO_LARGE_ERR_ST   | The horizontal size of the image block after SRM scaling exceeds 8191    |
| PPA_X_YUV420_RX_SCALE_ERR_ST    | The input descriptor parameters HA/hb/X happen to be odd numbers when the SRM input format is YUV420 |
| PPA_Y_YUV420_RX_SCALE_ERR_ST    | The input descriptor parameters VA/vb/Y happen to be odd numbers when the SRM input format is YUV420 |
| PPA_X_YUV420_TX_SCALE_ERR_ST    | The output descriptor parameters HA/hb/X happen to be odd numbers when the SRM output format is YUV420 |
| PPA_Y_YUV420_TX_SCALE_ERR_ST    | The output descriptor parameters VA/vb/Y happen to be odd numbers when the SRM output format is YUV420 |

Table 37.6-2. BLEND Parameter Error Types

| Error Type                     | Details                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| PPA_BLEND_SIZE_DIFF_ST          | The BLEND foreground and background sizes do not match                   |
| PPA_BLEND_YUV_X_SCALE_ERR_ST    | The BLEND background image format is YUV422 or YUV420, the horizontal size is an odd number |
| PPA_BLEND_YUV_Y_SCALE_ERR_ST    | The BLEND background image format is YUV420, the vertical size is an odd number |

37.7 Programming Procedures

37.7.1 PPA Clock Reset Configuration

1. Enable the clock of the PPA and 2D-DMA modules:
   * Write 1 to HP_SYS_CLKRST_PPA_SYS_CLK_EN to enable the PPA clock
   * Write 1 to HP_SYS_CLKRST_DMA2D_SYS_CLK_EN to enable the 2D-DMA clock

2. Reset the PPA and 2D-DMA modules:
   * Write 1 and then 0 to HP_SYS_CLKRST_RST_EN_PPA reset PPA
   * Write 1 and then 0 to HP_SYS_CLKRST_RST_EN_DMA2D reset 2D-DMA

37.7.2 SRM Configuration

1. Refer to Section 37.7.1 to enable and reset PPA and 2D-DMA.
2. Configure the inlink and outlink of 2D-DMA. For detailed parameters, please refer to Table 37.5-4.
```