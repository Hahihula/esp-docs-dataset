

```markdown
Register 8.58. LP_IO_MUX_GPIO{n}_REG (n: 0-6) (0x0000+0x4*n)

31                         18 17 16 15 14          12   11    10     9      8       7        6         5           4            3             2              1               0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0x1   2      0     0       0        0         0          0           0             0              0               Reset

LP_IO_MUX_GPIO{n}_MCU_OE Configures whether or not to enable the output of GPIO{n} during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIO{n}_SLP_SEL Configures whether or not to enable the sleep mode for GPIO{n}.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIO{n}_MCU_WPD Configures whether or not to enable the pull-down resistor of GPIO{n} during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIO{n}_MCU_WPU Configures whether or not to enable the pull-up resistor of GPIO{n} during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIO{n}_MCU_IE Configures whether or not to enable the input of GPIO{n} during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIO{n}_MCU_DRV Configures the drive strength of GPIO{n} during sleep mode.
O: ~5 mA
1: ~10 mA
2: ~20 mA
3: ~40 mA
(R/W)
```
Continued on the next page...
```