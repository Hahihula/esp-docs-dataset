

```markdown
Register 6.51. LP_GPIO_PINn_REG (n: 0-6) (0x0030+0x4*n)

Continued from the previous page...

LP_GPIO_PINn_WAKEUP_ENABLE Configures whether or not to enable GPIO n wake-up function.
O: Not enable
1: Enable

This function is disabled when PD_LP_PERI is powered off. For more information, see Chapter Low-Power Management.
(R/W)
```

```markdown
Register 6.52. LP_GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0-6) (0x02B0+0x4*n)

LP_GPIO_FUNCn_OUT_INV_SEL Configures whether or not to invert the output value.
O: Not invert
1: Invert
(R/W)

LP_GPIO_FUNCn_OE_INV_SEL Configures whether or not to invert the output enable signal.
O: Not invert
1: Invert
(R/W)
```

```markdown
Register 6.53. LP_GPIO_CLOCK_GATE_REG (0x03F8)

LP_GPIO_CLK_EN Configure to enable the GPIO clock gate or not.
O: Not enable
1: Enable
(R/W)
```