

```markdown
Register 9.29. GPIO_FUNCn_IN_SEL_CFG_REG (n: 0 - 255) (0x015C+4*n)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30-2 | GPIO_FUNCn_IN_SEL           |
|     |                              |
| 7   | GPIO_SIGn_IN_SEL            |
| 6   | GPIO_FUNn_IN_INV_SEL        |
| 5   | GPIO_FUNn_IN_SEL            |
| 4   | (reserved)                  |
| 3-0 | Reset                       |

GPIO_FUNCn_IN_SEL Configures to select a pin from the 55 GPIO pins to connect the input signal n.
0: Select GPIO0
1: Select GPIO1
......
53: Select GPIO53
54: Select GPIO54
55 ~ 61: invalid
Or
62: A constantly low input
63: A constantly high input
(R/W)

GPIO_FUNCn_IN_INV_SEL Configures whether or not to invert the input value.
0: Not invert
1: Invert
(R/W)

GPIO_SIGn_IN_SEL Configures whether or not to route signals via HP GPIO matrix.
0: Bypass HP GPIO matrix, i.e., connect signals directly to peripheral configured in HP IO MUX.
1: Route signals via HP GPIO matrix.
(R/W)
```