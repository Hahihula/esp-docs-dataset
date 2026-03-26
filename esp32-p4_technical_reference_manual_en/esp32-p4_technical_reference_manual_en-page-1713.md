

```markdown
Register 36.79. ISP_HIST_OFFS_REG (0x01AC)

| 31 | 28 | 27 |        ISP_HIST_X_OFFS         | 16 | 15 | 12 | 11 |          ISP_HIST_Y_OFFS           |
|----:|----:|----:|-------------------------------:|----:|----:|----:|----:|-------------------------------------|
|    |    |    |                               |    |    |    |    |                                     |
| O  | O  | O  |                               | O  | O  | O  | O  | Reset                              |

ISP_HIST_Y_OFFS Configures the start coordinate of the HIST statistics window in the vertical direction. (R/W)

ISP_HIST_X_OFFS Configures the start coordinate of the HIST statistics window in the horizontal direction. (R/W)


Register 36.80. ISP_HIST_SIZE_REG (0x01B0)

| 31 | 25 | 24 |        ISP_HIST_X_SIZE         | 16 | 15 | 9 | 8 |          ISP_HIST_Y_SIZE           |
|----:|----:|----:|-------------------------------:|----:|----:|---:|---:|-------------------------------------|
|    |    |    |                               |    |    | O | O |                                     |
| O  | O  | O  |                               | O  | O  | O | O | Reset                              |

ISP_HIST_Y_SIZE Configures the vertical dimension of the HIST sub-window. (R/W)

ISP_HIST_X_SIZE Configures the horizontal dimension of the HIST sub-window. (R/W)


Register 36.81. ISP_HIST_SEGO_REG (0x01B4)

| 31 | 24 | 23 |        ISP_HIST_SEG_0_1         | 16 | 15 | 8 | 7 |          ISP_HIST_SEG_3_4           |
|----:|----:|----:|-------------------------------:|----:|----:|---:|---:|-------------------------------------|
|    |    |    |                               | O  | O  | O | O | Reset                              |

ISP_HIST_SEG_3_4 Configures the threshold between the HIST interval 3 and 4. (R/W)

ISP_HIST_SEG_2_3 Configures the threshold between the HIST interval 2 and 3. (R/W)

ISP_HIST_SEG_1_2 Configures the threshold between the HIST interval 1 and 2. (R/W)

ISP_HIST_SEG_0_1 Configures the threshold between the HIST interval 0 and 1. (R/W)
```