

```markdown
Chapter 31 Pulse Count Controller (PCNT)

Register 31.4. PCNT_CTRL_REG (0x0060)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | PCNT_CLK_EN | (reserved) |
|     |    |    |    |    |    |    |    |    |    |    |    | 0 | 1 | 2 | 3 | 4 | 5 |
|     |    |    |    |    |    |    |    |    |    |    |    | 6 | 7 | (reserved) | PCNT_CNT_PAUSE_U3 | PCNT_PULSE_CNT_RST_U3 |
|     |    |    |    |    |    |    |    |    |    |    |    | 8 | 9 | 10 | PCNT_PULSE_CNT_U2 | PCNT_PULSE_CNT_U1 |
|     |    |    |    |    |    |    |    |    |    |    |    | 11 | 12 | 13 | PCNT_PULSE_CNT_U0 | Reset |

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

Register 31.5. PCNT_Un_CNT_REG (n: 0-3) (0x0030+0x4*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | PCNT_PULSE_CNT_U0 |
|     |    |    |    |    |    |    |    |    |    |    |    | 0x00 | Reset |

PCNT_PULSE_CNT_Un Represents the current pulse count value for unit n. (RO)
```