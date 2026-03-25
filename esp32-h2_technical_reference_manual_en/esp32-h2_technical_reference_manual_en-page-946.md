

```markdown
Chapter 32 Pulse Count Controller (PCNT)

Register 32.4. PCNT_CTRL_REG (0x0060)
| Bit | 31 | 30 | 29 | ... | 17 | 16 | 15 | reserved | reserved | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|-----|----|----|----|----------|----------|---|---|---|---|---|---|---|---|---|
|     |    |    |    |     |    | PCNT_CLK_EN | (reserved) |          | PONT_CNT_PAUSE_RST_U3 | PONT_CNT_PAUSE_RST_U2 | PONT_CNT_PAUSE_RST_U1 | PONT_CNT_PAUSE_RST_U0 |
| 0   | 0  | 0  | 0  | ... | 0  | 0  | 0  | 0        | 0        | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | Reset |

PCNT_PULSE_CNT_RST_Un Write 1 to clear unit n's counter.
O: No effect
1: Clear
(R/W)

PCNT_CNT_PAUSE_Un Write 1 to freeze unit n's counter.
O: No effect
1: Freeze
(R/W)

PCNT_CLK_EN Configures whether or not to enable the registers clock gate of the PCNT module.
O: The clock for registers is enabled when registers are read and written
1: The clock for registers is always on
(R/W)

Register 32.5. PCNT_Un_CNT_REG (n: 0-3) (0x0030+0x4*n)
| Bit | 31 | 16 | 15 | 0 |
|-----|----|----|----|---|
|     |    |    |    | Ox00 Reset |

PCNT_PULSE_CNT_Un Represents the current pulse count value for unit n. (RO)

GoBack
```
Espressif Systems
946
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```