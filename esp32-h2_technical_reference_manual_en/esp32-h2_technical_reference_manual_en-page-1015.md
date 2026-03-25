

```markdown
Register 34.2. TWAI_BUS_TIMING_O_REG (0x0018)

| Bit | Description                  |
|-----|------------------------------|
| 16-15| TWAI_SYNC_JUMP_WIDTH        |
| 14-0 | reserved                    |
|     | TWAI_BAUD_PRESC             |
| Reset| 0x00                       |

TWAI_BAUD_PRESC Configures baud rate prescaler value, determining the frequency dividing ratio.
O: Low
1: High
(RO | R/W)

TWAI_SYNC_JUMP_WIDTH Configures Synchronization Jump Width (SJW), ranging from 1 ~ 4 Tq wide. (RO | R/W)


Register 34.3. TWAI_BUS_TIMING_1_REG (0x001C)

| Bit | Description                  |
|-----|------------------------------|
| 7-0 | reserved                    |
| 8   | TWAI_TIME_SEG2              |
| 9   | TWAI_TIME_SEG1              |
| 10  | TWAI_TIME_SEG2              |
| 11  | TWAI_TIME_SEG1              |
| Reset| 0x0                        |

TWAI_TIME_SEG1 Configures the width of PBS1. (RO | R/W)

TWAI_TIME_SEG2 Configures the width of PBS2. (RO | R/W)

TWAI_TIME_SAMP Configures the number of sample points.
O: The bus is sampled once
1: The bus is sampled three times
(RO | R/W)
```