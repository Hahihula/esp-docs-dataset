

```markdown
Chapter 16 Permission Control (PMS)

Register 16.30. LP_APM_MO_STATUS_REG (0x00C8)
```

| bit | description |
|-----|-------------|
| 31-2 | (reserved) |
| 2   | LP_APM_MO_EXCEPTION_STATUS<br>bit0: 1 represents authority_exception<br>bit1: 1 represents space_exception<br>(RO) |

```markdown
Register 16.31. LP_APM_MO_STATUS_CLR_REG (0x00CC)
```

| bit | description |
|-----|-------------|
| 31-1 | (reserved) |
| 1   | LP_APM_MO_REGION_STATUS_CLR<br>Configures to clear exception status. (WT) |

```markdown
Register 16.32. LP_APM_MO_EXCEPTION_INFO0_REG (0x00D0)
```

| bit range | description |
|-----------|-------------|
| 31-23     | (reserved) |
| 22        | LP_APM_MO_EXCEPTION_ID<br>(RO) |
| 18-16     | LP_APM_MO_EXCEPTION_MODE<br>(RO) |
| 4-3        | LP_APM_MO_EXCEPTION_REGION<br>(RO) |
| 0          | Reset |

```markdown
LP_APM_MO_EXCEPTION_REGION Represents exception region. (RO)
LP_APM_MO_EXCEPTION_MODE Represents exception mode. (RO)
LP_APM_MO_EXCEPTION_ID Represents exception id information. (RO)

Espressif Systems    584    ESP32-C6 TRM (Version 1.1)
```