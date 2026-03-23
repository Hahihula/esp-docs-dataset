

```markdown
Register 14.62. PMS_DMA_APBPERI_PMS_MONITOR_2_REG (0x0088)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 27  |                                                                             |
| 26  |                                                                             |
| ... |                                                                             |
| 3   |                                                                             |
| 2   |                                                                             |
| 1   |                                                                             |
| 0   | Reset                                                                       |

PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_INTR Stores unauthorized DMA access interrupt status. (RO)

PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_ADDR Stores the address that triggered the unauthorized DMA address. Note that this is an offset to `0x3c000000` and the unit is 16, which means the actual address should be `0x3c000000 + PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_ADDR * 16`. (RO)
```