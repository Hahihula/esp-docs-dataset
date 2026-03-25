

```markdown
Register 16.38. CPU_APM_REGIONn_ADDR_START_REG (n: 0-7) (0x0004+0xC*n)

| 31           | 19   | 18          | 12 | 11             | 0               |
|--------------|------|-------------|----|----------------|-----------------|
|              |      | CPU_APM_REGIONn_ADDR_START_H |    |                |                 |
| Ox810        |      |             |    |                | Reset           |
|              |      |             |    | 0x0            |                 |

CPU_APM_REGIONn_ADDR_START_L Indicates the lower 12 bits of the start address of region n. (HRO)

CPU_APM_REGIONn_ADDR_START Configures the start address of region n. (R/W)

CPU_APM_REGIONn_ADDR_START_H Indicates the higher 13 bits of the start address of region n. (HRO)

Register 16.39. CPU_APM_REGIONn_ADDR_END_REG (n: 0-7) (0x0008+0xC*n)

| 31           | 19   | 18          | 12 | 11             | 0               |
|--------------|------|-------------|----|----------------|-----------------|
|              |      | CPU_APM_REGIONn_ADDR_END_H    |    |                |                 |
| Ox810        |      |             |    |                | Reset           |
|              |      |             |    | 0x7f          |                 |
|              |      |             |    | 0xff          |                 |

CPU_APM_REGIONn_ADDR_END_L Indicates the lower 12 bits of the end address of region n. (HRO)

CPU_APM_REGIONn_ADDR_END Configures the end address of region n. (R/W)

CPU_APM_REGIONn_ADDR_END_H Indicates the higher 13 bits of the end address of region n. (HRO)
```