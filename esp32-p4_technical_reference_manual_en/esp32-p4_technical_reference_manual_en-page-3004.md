

```markdown
Register 60.20. LP_ANA_TOUCH_SLP0_REG (0x011C)

| Bit | Field Name                     |
|-----|--------------------------------|
| 31  | (reserved)                    |
| 21  | LP_ANA_TOUCH_SLP_THO          |
| 20  |                                |
| 17  | LP_ANA_TOUCH_SLP_PAD          |
| 16  | LP_ANA_TOUCH_SLP_CHANNEL_CLR  |
| 15  |                                |
| 8   | Oxf                           |
| 7   | 0                             |
| 3   | Reset                         |

LP_ANA_TOUCH_SLP_THO Configures the touch threshold for sampling frequency mode 0 in sleep mode. (R/W)

LP_ANA_TOUCH_SLP_CHANNEL_CLR Write 1 to clear the benchmark data in sleep mode. (WT)

LP_ANA_TOUCH_SLP_PAD Configures which touch sensor to enter sleep mode. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.
0: No effect
1: Selects the touch sensor to enter sleep mode
(R/W)

Register 60.21. LP_ANA_TOUCH_SLP1_REG (0x0120)

| Bit | Field Name                     |
|-----|--------------------------------|
| 31  | (reserved)                    |
| 16  | LP_ANA_TOUCH_SLP_TH1          |
| 15  |                                |
| 8   | O                             |
| 7   | 0                             |
| 3   | Reset                         |

LP_ANA_TOUCH_SLP_TH2 Configures the touch threshold for sampling frequency mode 2 in sleep mode. (R/W)

LP_ANA_TOUCH_SLP_TH1 Configures the touch threshold for sampling frequency mode 1 in sleep mode. (R/W)
```