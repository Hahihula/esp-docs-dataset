

```markdown
Register 42.44. LP_UART_CLKDIV_SYNC_REG (0x0014)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 24  | LP_UART_CLKDIV_FRAG          |
| 23  |                              |
| 20  |                              |
| 19  |                              |
| 12  | (reserved)                   |
| 11  |                              |
| 8   | LP_UART_CLKDIV               |
| 7   |                              |
| 0   | Reset                        |

LP_UART_CLKDIV Configures the integral part of the divisor for baud rate generation. (R/W)
LP_UART_CLKDIV_FRAG Configures the fractional part of the divisor for baud rate generation. (R/W)

Register 42.45. LP_UART_RX_FILT_REG (0x0018)

| Bit | Description                                      |
|-----|--------------------------------------------------|
| 31  | (reserved)                                       |
| 9   | LP_UART_GLITCH_FILT_EN                          |
| 8   | LP_UART_GLITCH_FILT                              |
| 7   |                                                  |
| 0   | Reset                                            |

LP_UART_GLITCH_FILT Configures the width of a pulse to be filtered.
Measurement unit: UART Core’s clock cycle.
Pulses whose width is lower than this value will be ignored. (R/W)

LP_UART_GLITCH_FILT_EN Configures whether or not to enable RX signal filter.
0: Disable
1: Enable
(R/W)
```