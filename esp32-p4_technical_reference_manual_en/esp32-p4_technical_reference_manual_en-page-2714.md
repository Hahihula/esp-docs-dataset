

```markdown
## Register 53.3. TWAI_BUS_TIMING_O_REG (0x0018)

| Bit | Description |
|-----|-------------|
| 16-14 | TWAI_SYNC_JUMP_WIDTH Configures Synchronization Jump Width (SJW), ranging from 1 ~ 4 Tq wide. (R/W) |
| 13   | TWAI_BAUD_PRESC Configures baud rate prescaler value, determining the frequency dividing ratio.<br>0: Low<br>1: High<br>(R/W) |

## Register 53.4. TWAI_BUS_TIMING_1_REG (0x001C)

| Bit | Description |
|-----|-------------|
| 7-6 | TWAI_TIME_SEGMENT2 Configures the width of PBS2. (R/W) |
| 5-4 | TWAI_TIME_SEGMENT1 Configures the width of PBS1. (R/W) |
| 3   | TWAI_TIME_SAMPLING Configures the number of sample points.<br>0: The bus is sampled once<br>1: The bus is sampled three times<br>(R/W) |
```