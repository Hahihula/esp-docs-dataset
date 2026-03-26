

```markdown
Register 9.82. LP_IOMUX_PADn_REG (n = 0 - 15) (0x0008+4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30-12| LP_IOMUX_PADn_FILTER_EN, LP_IOMUX_PADn_FUN_SEL, LP_IOMUX_PADn_SLP_IE, LP_IOMUX_PADn_RDE, LP_IOMUX_PADn_RUE, LP_IOMUX_PADn_DRV, LP_IOMUX_PADn_MUX_SEL (bit order may vary per implementation) |
| 12-0 | Reset values: 0                                                             |

LP_IOMUX_PADn_DRV Configures the drive strength of GPIO n.
0: ~5 mA
1: ~10 mA
2: ~20 mA
3: ~40 mA
(R/W)

LP_IOMUX_PADn_RDE Configures whether or not enable pull-down resistor of GPIO n.
0: Disable
1: Enable
(R/W)

LP_IOMUX_PADn_RUE Configures whether or not to enable pull-up resistor of GPIO n.
0: Disable
1: Enable
(R/W)

LP_IOMUX_PADn_MUX_SEL Configures to decide GPIO n is used by HP IO MUX or LP IO MUX.
0: GPIO n is used by HP IO MUX
1: GPIO n is used by LP IO MUX
(R/W)

LP_IOMUX_PADn_FUN_SEL Configures to select LP IO MUX function for this signal.
0: Select Function 0
1: Select Function 1
......
(R/W)

LP_IOMUX_PADn_SLP_SEL Configures whether or not to enter sleep mode for GPIO n.
0: Not enter
1: Enter
(R/W)

LP_IOMUX_PADn_SLP_IE Configures whether or not to enable the input of GPIO n during sleep mode.
0: Disable
1: Enable
(R/W)
```