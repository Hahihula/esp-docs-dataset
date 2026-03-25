

```markdown
Register 18.57. CPU_APM_REGION_FILTER_EN_REG (0x0000)

| Bit | Description         |
|-----|---------------------|
| 31  | reserved            |
| 30  |                     |
| ... |                     |
| 8   |                     |
| 7   |                     |
| 6   |                     |
| 5   |                     |
| 4   |                     |
| 3   |                     |
| 2   |                     |
| 1   |                     |
| 0   | CPU_APM_REGION_FILTER_EN (Reset: 0x1) |

CPU_APM_REGION_FILTER_EN Configures bit n (0-7) to enable permission checks for region n (0-7).
O: Disable
1: Enable
(R/W)

Register 18.58. CPU_APM_REGIONn_ADDR_START_REG (n: 0-7) (0x0004+0xC*n)

| Bit | Description         |
|-----|---------------------|
| 31  |                     |
| ... |                     |
| 19  | CPU_APM_REGIONn_ADDR_START_H |
| 18  |                     |
| 17  |                     |
| 16  |                     |
| 15  |                     |
| 14  |                     |
| 13  |                     |
| 12  |                     |
| 11  |                     |
| 10  |                     |
| 9   |                     |
| 8   |                     |
| 7   |                     |
| 6   |                     |
| 5   |                     |
| 4   |                     |
| 3   |                     |
| 2   |                     |
| 1   |                     |
| 0   | CPU_APM_REGIONn_ADDR_START_L (Reset: 0x810) |

CPU_APM_REGIONn_ADDR_START_L Indicates the lower 12 bits of the start address of region n. (HRO)

CPU_APM_REGIONn_ADDR_START Configures the start address of region n. (R/W)

CPU_APM_REGIONn_ADDR_START_H Indicates the higher 13 bits of the start address of region n. (HRO)
```