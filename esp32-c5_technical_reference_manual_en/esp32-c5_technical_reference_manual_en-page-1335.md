

```markdown
Chapter 36 Pulse Count Controller (PCNT)

Register 36.5. PCNT_CTRL_REG (0x0070)
```

| Bit | Description |
|-----|-------------|
| 17  | PONT_CLK_EN  |
| 16  | (reserved)   |
| 12-8| PONT_DALTA_CHANGE_EN_U3 to PONT_DALTA_CHANGE_EN_U0 |
| 7   | PONT_CNT_PAUSE_U3 |
| 6   | PONT_CNT_PAUSE_U2 |
| 5   | PONT_CNT_PAUSE_U1 |
| 4   | PONT_CNT_PAUSE_U0 |
| 3   | PONT_PULSE_CNT_RST_U3 |
| 2   | PONT_PULSE_CNT_RST_U2 |
| 1   | PONT_PULSE_CNT_RST_U1 |
| 0   | PONT_PULSE_CNT_RST_U0 |

PCNT_PULSE_CNT_RST_Un (n: 0-3) Write 1 to clear unit n’s counter.
- 0: No effect
- 1: Clear
(R/W)

PCNT_CNT_PAUSE_Un (n: 0-3) Write 1 to freeze unit n’s counter.
- 0: No effect
- 1: Freeze
(R/W)

PCNT_DALTA_CHANGE_EN_Un (n: 0-3) Configures this bit to enable unit n’s step comparator. (R/W)

PCNT_CLK_EN Configures whether or not to enable the registers clock gate of the PCNT module.
- 0: The registers can not be read or written by application
- 1: The registers can be read and written by application
(R/W)

Register 36.6. PCNT_Un_CNT_REG (n: 0-3) (0x0040+0x4*n)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved)   |
| 16  | PONT_CLK_EN  |
| 15  | (reserved)   |
| 8-0 | PCNT_PULSE_CNT_Un |

PCNT_PULSE_CNT_Un Represents the current pulse count value for unit n. (RO)
```