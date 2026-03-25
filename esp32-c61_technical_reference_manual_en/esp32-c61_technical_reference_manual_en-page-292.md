

```markdown
Register 6.20. GPIO_FUNCt_IN_SEL_CFG_REG ( t: 72-74) (0x03F4+0x4*(t-72))
```

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
|    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset | GPIO_SIGt_IN_SEL | GPIO_FUNCt_IN_INV_SEL | GPIO_FUNCt_IN_SEL |

GPIO_FUNCt_IN_SEL Configures to select a pin from the 22 GPIO pins (GPIO0~GPIO13, GPIO22~GPIO29) to connect the input signal t.

- `0x0`: Select GPIO0
- `0x1`: Select GPIO1
- ...
- `0x1C`: Select GPIO28
- `0x1D`: Select GPIO29

Or

- `0x40`: A constantly high input
- `0x60`: A constantly low input (R/W)

GPIO_FUNCt_IN_INV_SEL Configures whether or not to invert the input value.

- `0`: Not invert
- `1`: Invert (R/W)

GPIO_SIGt_IN_SEL Configures whether or not to route signals via HP GPIO matrix.

- `0`: Bypass HP GPIO matrix, i.e., connect signals directly to peripheral configured in HP IO MUX.
- `1`: Route signals via HP GPIO matrix. (R/W)
```