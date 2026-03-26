

```markdown
Register 6.23. DMA2D_IN_COLOR_CONVERT_CHO_REG (0x054C)
```

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                         |                                                                             |
| 31  |                                         |                                                                             |
| 31  |                                         |                                                                             |
| ... | ...                                     | ...                                                                         |
| 6   |                                         | (reserved)                                                                  |
| 5   | DMA2D_IN_COLOR_INPUT_SEL_CHO           | Configures the first stage output of color space conversion for RX channel 0.|
| 4   | DMA2D_IN_COLOR_3B_PROC_EN_CHO           | Configures whether to enable the second stage of color space conversion for RX channel 0. |
| 3   |                                         |                                                                             |
| 2   |                                         |                                                                             |
| 1   |                                         |                                                                             |
| 0   | Reset                                   | 0x7 / 0x0                                                                    |

DMA2D_IN_COLOR_OUTPUT_SEL_CHO Configures the third stage output of color space conversion for RX channel 0.
- 0: RGB888 to RGB565
- 1: Output directly
(R/W)

DMA2D_IN_COLOR_3B_PROC_EN_CHO Configures whether to enable the second stage of color space conversion for RX channel 0.
- 0: Disable
- 1: Enable
(R/W)

DMA2D_IN_COLOR_INPUT_SEL_CHO Configures the first stage output of color space conversion for RX channel 0.
- 0: YUV422/420 to YUV444
- 1: YUV422
- 2: YUV444/420
- 7: Disable color space conversion
Others: Invalid
(R/W)
```