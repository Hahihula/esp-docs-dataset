

```markdown
Register 32.44. LP_UART_CLKDIV_SYNC_REG (0x0014)

LP_UART_CLKDIV Configures the integral part of the divisor for baud rate generation. (R/W)
LP_UART_CLKDIV_FRAG Configures the fractional part of the divisor for baud rate generation. (R/W)


Register 32.45. LP_UART_RX_FILT_REG (0x0018)

LP_UART_GLITCH_FILT Configures the width of a pulse to be filtered.
Measurement unit: UART Core's clock cycle.
Pulses whose width is lower than this value will be ignored. (R/W)

LP_UART_GLITCH_FILT_EN Configures whether or not to enable RX signal filter.
0: Disable
1: Enable
(R/W)
```