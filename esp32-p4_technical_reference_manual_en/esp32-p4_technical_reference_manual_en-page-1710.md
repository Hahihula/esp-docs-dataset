

```markdown
Register 36.74. ISP_COLOR_CTRL_REG (0x018C)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----|----|----|----|---|---|---|
| 0x0 |    |    | 0x80 |     |   |   | 0x80 |

ISP_COLOR_SATURATION Configures the saturation. Bit [7] is the integer part, and bits [6:0] are the fractional part. (R/W)

ISP_COLOR_HUE Configures the lower 8 bits of the hue value. The hue value is 9 bits in total, with the MSB provided by ISP_COLOR_HUE_H. Valid range: 0–359. (R/W)

ISP_COLOR_CONTRAST Configures the saturation. Bit [7] is the integer part, and bits [6:0] are the fractional part. (R/W)

ISP_COLOR_BRIGHTNESS Configures the brightness in two’s complement. (R/W)
```

```markdown
Register 36.75. ISP_BLC_VALUE_REG (0x0190)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----|----|----|----|---|---|---|
| 0   |    |    |     |     |   |   |     |

ISP_BLC_R3_VALUE Configures the black level offset of channel 3 in the Bayer image. (R/W)

ISP_BLC_R2_VALUE Configures the black level offset of channel 2 in the Bayer image. (R/W)

ISP_BLC_R1_VALUE Configures the black level offset of channel 1 in the Bayer image. (R/W)

ISP_BLC_R0_VALUE Configures the black level offset of channel 0 in the Bayer image. (R/W)
```