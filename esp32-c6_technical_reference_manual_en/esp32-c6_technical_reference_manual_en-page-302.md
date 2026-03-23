

```markdown
Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX) GoBack

Register 7.46. LP_IO_GPIOn_REG (n: 0-7) (0x0048+0x4*n)

Continued from the previous page...

LP_GPIO_GPIOn_MCU_IE Configures whether or not to enable the input of GPIO n during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_GPIO_GPIOn_MCU_RUE Configures whether or not to enable the pull-up resistor of GPIO n during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_GPIO_GPIOn_MCU_RDE Configures whether or not to enable the pull-down resistor of GPIO n during sleep mode.
O: Not enable
1: Enable
(R/W)

LP_GPIO_GPIOn_SLP_SEL Configures whether or not to enable the sleep mode for GPIO n.
O: Not enable
1: Enable
(R/W)

LP_GPIO_GPIOn_MCU_OE Configures whether or not to enable the output of GPIO n during sleep mode.
O: Not enable
1: Enable
(R/W)
```