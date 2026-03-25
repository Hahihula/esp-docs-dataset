

```markdown
Register 8.21. GPIO_FUNCu_IN_SEL_CFG_REG (u: 97-116) (0x0448+0x4*(u-97))

| bit | 31 | 30 | 29 | 28 | 27 | ... | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|-----|---|---|---|---|---|---|
|     |    |    |    |    |    |      |   |   |   |   |   | Reset (0x60) |

GPIO_FUNCu_IN_SEL Configures to select a pin from the 21 GPIO pins (GPIO0~GPIO14, GPIO23~GPIO28) to connect the input signal u.
- 0x0: Select GPIO0
- 0x1: Select GPIO1
...
- 0x1B: Select GPIO27
- 0x1C: Select GPIO28

Or
- 0x40: A constantly high input
- 0x60: A constantly low input (R/W)

GPIO_FUNCu_IN_INV_SEL Configures whether or not to invert the input value.
- 0: Not invert
- 1: Invert (R/W)

GPIO_SIGu_IN_SEL Configures whether or not to route signals via GPIO matrix.
- 0: Bypass GPIO matrix, i.e., connect signals directly to peripheral configured in IO MUX.
- 1: Route signals via GPIO matrix. (R/W)
```