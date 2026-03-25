

```markdown
Register 25.7. UART_CLKDIV_SYNC_REG (0x0014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    | (reserved) | UART_CLKDIV_FRAG | UART_CLKDIV | (reserved) | UART_CLKDIV |
| Value | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x2b6 |

UART_CLKDIV Configures the integral part of the divisor for baud rate generation. (R/W)
UART_CLKDIV_FRAG Configures the fractional part of the divisor for baud rate generation. (R/W)

Register 25.8. UART_RX_FILT_REG (0x0018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    | (reserved) | UART_GLITCH_FILT_EN | UART_GLITCH_FILT_EN | UART_GLITCH_FILT | UART_GLITCH_FILT |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x8 |

UART_GLITCH_FILT Configures the width of a pulse to be filtered.
Measurement unit: UART Core's clock cycle.
Pulses whose width is lower than this value will be ignored. (R/W)

UART_GLITCH_FILT_EN Configures whether or not to enable RX signal filter.
0: Disable
1: Enable
(R/W)
```