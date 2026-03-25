

```markdown
Register 18.59. CPU_APM_REGIONn_ADDR_END_REG (n: 0-7) (0x0008+0xC*n)

| 31           | 19   | 18       | 12   | 11     | 0      |
|--------------|------|----------|------|--------|--------|
|              | 0x810|          | Ox7f |        | Reset  |
|              |      |          |      |        |        |

CPU_APM_REGIONn_ADDR_END_L Indicates the lower 12 bits of the end address of region n. (HRO)

CPU_APM_REGIONn_ADDR_END Configures the end address of region n. (R/W)

CPU_APM_REGIONn_ADDR_END_H Indicates the higher 13 bits of the end address of region n. (HRO)
```