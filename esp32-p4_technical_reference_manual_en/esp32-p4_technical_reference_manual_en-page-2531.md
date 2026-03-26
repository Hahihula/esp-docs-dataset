

```markdown
Chapter 48 Pulse Count Controller (PCNT)

Register 48.4. PCNT_CTRL_REG (0x0060)
| 31 | 17 | 16 | 15 | (reserved) | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|------------:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
|    |    | PCNT_CLK_EN | (reserved) | PONT_CNT_PAUSE_U3 | PONT_PULSE_CNT_RST_U3 | PONT_PULSE_CNT_U2 | PONT_PULSE_CNT_U1 | Reset |
0 0 0 0 0 0 0 0 0 0 0 0 0 0

PCNT_PULSE_CNT_RST_Un Write 1 to clear unit n's counter.
O: No effect
1: Clear
(R/W)

PCNT_CNT_PAUSE_Un Write 1 to freeze unit n's counter.
O: No effect
1: Freeze
(R/W)

PCNT_CLK_EN Configures whether or not to enable the registers clock gate of PCNT module.
O: the clock for registers is enabled when registers are read and written
1: the clock for registers is always on
(R/W)

Register 48.5. PCNT_Un_CNT_REG (n: 0-3) (0x0030+0x4*n)
| 31 | 16 | 15 | 0 |
|----:|----:|----:|---:|
|    |    | Ox00 | Reset |

PCNT_PULSE_CNT_Un Represents the current pulse count value for unit n. (RO)

Espressif Systems
2531
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```