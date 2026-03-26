

```markdown
| Signal No. | Input Signal | Default value | Direct Input via LP IO MUX | Output Signal | Output enable signal when LP_GPIO_FUNCn_OE_SEL = 0 | Direct Output via LP IO MUX |
|------------|--------------|---------------|-----------------------------|---------------|--------------------------------------------------|------------------------------|
| 24         | -            | -             | -                           | -             | -                                                | -                            |
| 25         | -            | -             | -                           | -             | -                                                | -                            |
| 26         | -            | -             | -                           | -             | -                                                | -                            |
| 27         | -            | -             | -                           | -             | -                                                | -                            |
| 28         | -            | -             | -                           | -             | -                                                | -                            |
| 29         | -            | -             | -                           | -             | -                                                | -                            |
| 30         | -            | -             | -                           | -             | -                                                | -                            |
| 31         | -            | -             | -                           | -             | -                                                | -                            |

## 9.14 HP IO MUX Functions List

Table 9.14-1 shows the HP IO MUX functions and default states of each HP GPIO pin.

Table 9.14-1. HP IO MUX Pin Functions

| Name   | Function 0 | Function 1 | Function 2 | Function 3 | DRV | Reset | Notes |
|--------|------------|------------|------------|------------|-----|-------|-------|
| GPIO0  | GPIO0      | GPIO0      | -          | -          | 2   | 0     | R     |
| GPIO1  | GPIO1      | GPIO1      | -          | -          | 2   | 0     | R     |
| GPIO2  | MTCK       | GPIO2      | -          | -          | 2   | 1*    | R     |
| GPIO3  | MTDI       | GPIO3      | -          | -          | 2   | 1     | R     |
| GPIO4  | MTMS       | GPIO4      | -          | -          | 2   | 1     | R     |
| GPIO5  | MTDO       | GPIO5      | -          | -          | 2   | 0     | R     |
| GPIO6  | GPIO6      | GPIO6      | -          | SPI2_HOLD_PAD | 2   | 0     | R     |
| GPIO7  | GPIO7      | GPIO7      | -          | SPI2_CS_PAD  | 2   | 0     | R     |
| GPIO8  | GPIO8      | GPIO8      | UARTO_RTS_PAD | SPI2_D_PAD    | 2   | 0     | R     |

Cont'd on next page
```