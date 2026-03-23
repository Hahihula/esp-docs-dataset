

```markdown
Register 33.2. TWAI_BUS_TIMING_O_REG (0x0018)

| Bit | Field Name               | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 16  | TWAI_SYNC_JUMP_WIDTH     | Configures Synchronization Jump Width (SJW), ranging from 1 ~ 4 Tq wide.    |
| 15  |                          |                                                                             |
| 14  |                          |                                                                             |
| 13  |                          |                                                                             |
| 0x0 | TWAI_BAUD_PRESC          | Configures baud rate prescaler value, determining the frequency dividing ratio.<br>0: Low<br>1: High<br>(RO | R/W) |

Register 33.3. TWAI_BUS_TIMING_1_REG (0x001C)

| Bit | Field Name               | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 7   |                          |                                                                             |
| 6   |                          |                                                                             |
| 4   | TWAI_TIME_SEG2           | Configures the width of PBS2. (RO | R/W)                                   |
| 3   | TWAI_TIME_SEG1           | Configures the width of PBS1. (RO | R/W)                                   |
| 2   |                          |                                                                             |
| 1   | TWAI_TIME_SAMP           | Configures the number of sample points.<br>0: The bus is sampled once<br>1: The bus is sampled three times<br>(RO | R/W) |
```