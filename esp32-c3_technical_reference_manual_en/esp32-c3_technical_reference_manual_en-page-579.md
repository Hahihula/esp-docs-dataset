

```markdown
Register 26.6. UART_INT_CLR_REG (0x0010)

Continued from the previous page...

UART_RS485_FRM_ERR_INT_CLR Set this bit to clear the UART_RS485_FRM_ERR_INT interrupt.
(WT)

UART_RS485_CLASH_INT_CLR Set this bit to clear the UART_RS485_CLASH_INT interrupt. (WT)

UART_AT_CMD_CHAR_DET_INT_CLR Set this bit to clear the UART_AT_CMD_CHAR_DET_INT inter-
rupt. (WT)

UART_WAKEUP_INT_CLR Set this bit to clear the UART_WAKEUP_INT interrupt. (WT)


Register 26.7. UART_CLKDIV_REG (0x0014)
```
```markdown
| Bit Range | Description                  |
|-----------|------------------------------|
| 31-24     | (reserved)                   |
| 23        | UART_CLKDIV_FRAG              |
| 20-19     | (reserved)                   |
| 12-11     | UART_CLKDIV                  |
| 10-0      | Reset                        |

UART_CLKDIV The integral part of the frequency divisor. (R/W)

UART_CLKDIV_FRAG The fractional part of the frequency divisor. (R/W)
```
```markdown
Register 26.8. UART_RX_FILT_REG (0x0018)

| Bit Range | Description                  |
|-----------|------------------------------|
| 31-7      | (reserved)                   |
| 6-0       | Reset                        |

UART_GLITCH_FILT When input pulse width is lower than this value, the pulse is ignored. (R/W)

UART_GLITCH_FILT_EN Set this bit to enable RX signal filter. (R/W)
```