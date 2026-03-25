

```markdown
Chapter 36 Pulse Count Controller (PCNT)

Register 36.10. PCNT_INT_ENA_REG (0x0058)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 4   | 3       | 2       | 1       | 0        | Reset                                                |
|     |         |         |         |          |                                                         |
|     | PCNT_CNT_THR_EVENT_UN_INT_ENA(n: 0-3) | The interrupt enable bit for the PCNT_CNT_THR_EVENT_Un_INT interrupt. (R/W) |

```markdown
Register 36.11. PCNT_INT_CLR_REG (0x005C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 4   | 3       | 2       | 1       | 0        | Reset                                                |
|     |         |         |         |          |                                                         |
|     | PCNT_CNT_THR_EVENT_UN_INT_CLR(n: 0-3) | Write 1 to clear the PCNT_CNT_THR_EVENT_Un_INT interrupt. (WT) |

```markdown
Register 36.12. PCNT_DATE_REG (0x00FC)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
|     |                                 | 0x2407310                                                                   |
|     |                                 | Reset                                                                      |
|     | PCNT_DATE                      | Version control register. (R/W)                                            |

```markdown
Espressif Systems

Submit Documentation Feedback

ESP32-C5 TRM (Version 1.0)
```