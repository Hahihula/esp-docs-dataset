

```markdown
Register 38.3. LCD_CAM_LCD_USER_REG (0x0014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 14 | 13 | 12 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |    |    |    | Ox01 Reset |

LCD_CAM_LCD_DOUT_CYCLELEN Configures the period of the LCD module's data output phase (DOUT). The actual period duration = the value of this field + 1. (R/W)

LCD_CAM_LCD_ALWAYS_OUT_EN Enables continuous output of the LCD module. In this mode, the LCD module continuously outputs data during the DOUT phase, until `LCD_CAM_LCD_START` is cleared or `LCD_CAM_LCD_RESET` is set. (R/W)

LCD_CAM_LCD_DOUT_BYTE_SWIZZLE_MODE Configures LCD output data byte reordering. For details please refer to Table 38.3-3. (R/W)

LCD_CAM_LCD_DOUT_BYTE_SWIZZLE_ENABLE Configures whether to enable LCD output data byte reordering.
0: Disable
1: Enable
(R/W)

LCD_CAM_LCD_DOUT_BIT_ORDER Configures whether to invert the LCD output data bit order.
0: Do not invert.
1: Invert the bit order. In n-bit mode, `LCD_DATA_in[n-1:0]` is inverted to `LCD_DATA_in[0:n-1]`.
(R/W)

LCD_CAM_LCD_BYTE_MODE Configures the data bit width from GDMA.
0: 8-bit
1: 16-bit
2: 24-bit
(R/W)

LCD_CAM_LCD_UPDATE Configures whether to update the LCD register configurations.
0: Do not update.
1: Update configurations. This bit is cleared by hardware.
(R/W)

LCD_CAM_LCD_BIT_ORDER Configures whether to invert the bit order of the LCD input data.
0: Do not invert.
1: Invert the bit order. In n-bit mode, `LCD_DATA_in[n-1:0]` is inverted to `LCD_DATA_in[0:n-1]`.
(R/W)
```