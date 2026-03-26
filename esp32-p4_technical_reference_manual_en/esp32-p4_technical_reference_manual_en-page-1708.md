

```markdown
Register 36.68. ISP_AWB_MODE_REG (0x0164)

| Bit | Description         |
|-----|---------------------|
| 5   | ISP_AWB_SAMPLE      |
| 4   | (reserved)          |
| 3   |                     |
| 2   |                     |
| 1   |                     |
| 0   | ISP_AWB_MODE        |

ISP_AWB_MODE Configures whether to enable the AWB algorithm.
1: Enable
Others: Invalid
(R/W)

ISP_AWB_SAMPLE Configures the AWB sampling point.
0: Use data output before processed by CCM
1: Use data output after processed by CCM
(R/W)

Register 36.69. ISP_AWB_HSCALE_REG (0x0168)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 28  |                     |
| 27  |                     |
| 16  | ISP_AWB_LPOINT      |
| 15  | (reserved)          |
| 12  |                     |
| 11  |                     |
| 0   | ISP_AWB_RPOINT      |

ISP_AWB_RPOINT Configures the right boundary coordinate of the AWB statistical window. (R/W)
ISP_AWB_LPOINT Configures the left boundary coordinate of the AWB statistical window. (R/W)

Register 36.70. ISP_AWB_VSCALE_REG (0x016C)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 28  |                     |
| 27  |                     |
| 16  | ISP_AWB_TPOINT      |
| 15  | (reserved)          |
| 12  |                     |
| 11  |                     |
| 0   | ISP_AWB_BPOINT      |

ISP_AWB_BPOINT Configures the bottom boundary coordinate of the AWB statistical window. (R/W)
ISP_AWB_TPOINT Configures the top boundary coordinate of the AWB statistical window. (R/W)
```