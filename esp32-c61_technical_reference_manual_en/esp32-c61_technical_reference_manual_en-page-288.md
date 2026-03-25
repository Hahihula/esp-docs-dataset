
```markdown
Register 6.15. GPIO_PINn_REG (n: 0-29) (0x00D4+0x4*n)

Continued from the previous page...

GPIO_PINn_INT_ENA Configures whether or not to enable CPU interrupt or CPU non-maskable interrupt.
- Bit[13]: Configures whether or not to enable the GPIO_EXT_REG_INT interrupt:
  O: Disable
  1: Enable
- Bit[14]: Invalid
- Bit[15]: Configures whether or not to enable the GPIO_SDIO_INT interrupt
- Bit[16]~bit[17]: Invalid
(R/W)

Register 6.16. GPIO_FUNCm_IN_SEL_CFG_REG (m: 6-17) (0x02D4+0x4*(m-6))

GPIO_FUNCm_IN_SEL Configures to select a pin from the 22 GPIO pins (GPIO0~GPIO13, GPIO22~GPIO29) to connect the input signal m.
0x0: Select GPIO0
0x1: Select GPIO1
......
0x1C: Select GPIO28
0x1D: Select GPIO29
Or
0x40: A constantly high input
0x60: A constantly low input
(R/W)

GPIO_FUNCm_IN_INV_SEL Configures whether or not to invert the input value.
O: Not invert
1: Invert
(R/W)

GPIO_SIGm_IN_SEL Configures whether or not to route signals via HP GPIO matrix.
O: Bypass HP GPIO matrix, i.e., connect signals directly to peripheral configured in HP IO MUX.
1: Route signals via HP GPIO matrix.
(R/W)
```