

```markdown
Register 7:15. GPIO_FUNCn_IN_SEL_CFG_REG (n: 0-127) (0x0154+4*n)

| 31 | 30 | 29 | ... | 2 | 1 | 0 |
|----|----|----|-----|---|---|---|
| 0  | 0  | 0  | ... | 0 | 0 | 0 |

GPIO_FUNCn_IN_SEL   Configures to select a pin from the 31 GPIO pins to connect the input signal n.
0: Select GPIO0
1: Select GPIO1
......
29: Select GPIO29
30: Select GPIO30
Or
0x38: A constantly high input
0x3C: A constantly low input
(R/W)

GPIO_FUNCn_IN_INV_SEL   Configures whether or not to invert the input value.
0: Not invert
1: Invert
(R/W)

GPIO_SIGn_IN_SEL   Configures whether or not to route signals via GPIO matrix.
0: Bypass GPIO matrix, i.e., connect signals directly to peripheral configured in IO MUX.
1: Route signals via GPIO matrix.
(R/W)
```