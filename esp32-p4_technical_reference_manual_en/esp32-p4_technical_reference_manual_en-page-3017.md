

# 61.9 Registers

The addresses in this section are relative to Temperature Sensor base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 61.1. TSENS_CTRL_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  |    | TSENS_POWER_UP | TSENS_CLK_DIV | (reserved) | TSENS_IN_INV | (reserved) | TSENS_SAMPLE_EN | (reserved) | TSENS_OUT |
|     |    |    |    |    |    |    |    | Ox6 |                |               |             |            | Reset       |             |           |

**TSENS_OUT** Stores the temperature sensor output value. (RO)

**TSENS_SAMPLE_EN** Configures whether to enable automatic temperature monitoring.
- 0: Disable
- 1: Enable
(R/W)

**TSENS_IN_INV** Configures whether to invert temperature sensor data.
- 0: No effect
- 1: Invert
(R/W)

**TSENS_CLK_DIV** Configures the clock division of the temperature sensor, which affects the frequency of temperature data generation by the analog circuits. (R/W)

**TSENS_POWER_UP** Configures whether to power up temperature sensor.
- 0: No effect
- 1: Power up
(R/W)