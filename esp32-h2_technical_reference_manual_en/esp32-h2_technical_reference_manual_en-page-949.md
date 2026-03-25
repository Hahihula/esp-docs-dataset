

```markdown
Chapter 32 Pulse Count Controller (PCNT)

Register 32.10. PCNT_INT_CLR_REG (0x004C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 3   | PCNT_CNT_THR_EVENT_U3_INT_CLR  |                                                                             |
| 2   | PCNT_CNT_THR_EVENT_U2_INT_CLR  |                                                                             |
| 1   | PCNT_CNT_THR_EVENT_U1_INT_CLR  |                                                                             |
| 0   | PCNT_CNT_THR_EVENT_U0_INT_CLR  |                                                                             |

PCNT_CNT_THR_EVENT_Un_INT_CLR Write 1 to clear the PCNT_CNT_THR_EVENT_U_n_INT interrupt. (WO)

Register 32.11. PCNT_DATE_REG (0x00FC)
```

| Bit | Field Name     | Description |
|-----|-----------------|-------------|
| 31  |                | 0           |
|     | PCNT_DATE      |             |

PCNT_DATE Version control register. (R/W)

Espressif Systems
949
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```