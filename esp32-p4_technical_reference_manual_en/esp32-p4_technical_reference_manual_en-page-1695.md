

```markdown
Register 36.41. ISP_GAMMA_BX2_REG (0x00BC)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   | 0  | 0  | 0  | 0  | 0  | 0  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | 4  | Reset |

ISP_GAMMA_B_XOF Configures the width of the 15th interval on the X axis of B channel gamma curve. Refer to section 36.5.2.8 for configuration. (R/W)

ISP_GAMMA_B_XOE Configures the width of the 14th interval on the X axis of B channel gamma curve. (R/W)

ISP_GAMMA_B_XOD Configures the width of the 13th interval on the X axis of B channel gamma curve. (R/W)

ISP_GAMMA_B_XOC Configures the width of the 12th interval on the X axis of B channel gamma curve. (R/W)

ISP_GAMMA_B_XOB Configures the width of the 11th interval on the X axis of B channel gamma curve. (R/W)

ISP_GAMMA_B_XOA Configures the width of the 10th interval on the X axis of B channel gamma curve. (R/W)

ISP_GAMMA_B_XO9 Configures the width of the 9th interval on the X axis of B channel gamma curve. (R/W)

ISP_GAMMA_B_XO8 Configures the width of the 8th interval on the X axis of B channel gamma curve. (R/W)


Register 36.42. ISP_AE_CTRL_REG (0x00CO)
```
```markdown
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 2 |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

ISP_AE_UPDATE Configures AE statistics sampling. With AE enabled, writing 1 triggers a statistics collection. (WT)

ISP_AE_SELECT Configures the AE sampling point.
0: Use data output from the demosaic module
1: Use data output from the gamma correction module
(R/W)
```