

```markdown
Register 6.18. GPIO_FUNCq_IN_SEL_CFG_REG (q: 46-47) (0x038C+0x4*(q-46))

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 9   | GPIO_SIGq_IN_SEL                                                             |
| 8   | GPIO_FUNCq_IN_INV_SEL                                                       |
| 7   | GPIO_FUNCq_IN_SEL                                                             |
| 6   | O                                                                            |
| 0   | 0x60                                                                         |
|     | Reset                                                                        |

GPIO_FUNCq_IN_SEL Configures to select a pin from the 22 GPIO pins (GPIO0~GPIO13, GPIO22~GPIO29) to connect the input signal q.
- 0x0: Select GPIO0
- 0x1: Select GPIO1
- ...
- 0x1C: Select GPIO28
- 0x1D: Select GPIO29
Or
- 0x40: A constantly high input
- 0x60: A constantly low input
(R/W)

GPIO_FUNCq_IN_INV_SEL Configures whether or not to invert the input value.
- 0: Not invert
- 1: Invert
(R/W)

GPIO_SIGq_IN_SEL Configures whether or not to route signals via HP GPIO matrix.
- 0: Bypass HP GPIO matrix, i.e., connect signals directly to peripheral configured in HP IO MUX.
- 1: Route signals via HP GPIO matrix.
(R/W)
```