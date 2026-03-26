

```markdown
## Register 9.64. LP_GPIO_CLK_EN_REG (0x0000)

LP_GPIO_CLK_EN   Configures whether or not to enable clock gate.
O: Not enable
1: Enable, the clock is free running.
(R/W)
```

```markdown
## Register 9.65. LP_GPIO_VER_DATE_REG (0x0004)

LP_GPIO_VER_DATE Version control register.
(R/W)
```

```markdown
## Register 9.66. LP_GPIO_OUT_REG (0x0008)

LP_GPIO_OUT_DATA Configures the output value of GPIO0 ~ GPIO15 output in simple GPIO output mode.
O: Low level
1: High level
The value of bit0 ~ bit15 correspond to the output value of GPIO0 ~ GPIO15 respectively. Bit16 ~ bit31 are invalid.
(R/W/WTC)
```