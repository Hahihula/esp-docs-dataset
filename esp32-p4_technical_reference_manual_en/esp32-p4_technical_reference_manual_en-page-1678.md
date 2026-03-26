

```markdown
Register 36.15. ISP_DPC_CTRL_REG (0x0038)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 30  | ISP_DPC_CHECK_EN            | Configures whether to enable the static calibration function. Calibration and correction cannot be enabled at the same time.<br>0: Disable<br>1: Enable<br>(R/W) |
| 29  | ISP_STA_EN                  | Configures whether to enable the static correction function.<br>0: Disable<br>1: Enable<br>(R/W) |
| 28  | ISP_DYN_EN                  | Configures whether to enable the dynamic correction function.<br>0: Disable<br>1: Enable<br>(R/W) |
| 27  | ISP_DPC_BLACK_EN            | Configures the image type used for static calibration.<br>0: White image<br>1: Black image<br>(R/W) |
| 26  | ISP_DPC_METHOD_SEL          | Configures the algorithm selection for dynamic correction.<br>0: Select Algorithm 0<br>1: Select Algorithm 1<br>(R/W) |
| 25  | ISP_DPC_CHECK_OD_EN         | Configures whether to output image data during the static calibration process.<br>0: Do not output image<br>1: Output image<br>(R/W) |
```