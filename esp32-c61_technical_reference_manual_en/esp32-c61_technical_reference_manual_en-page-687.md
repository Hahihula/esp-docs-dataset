

```markdown
Register 16.12. HP_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | Reset |

HP_APM_M1_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M1_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_M1_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 16.13. HP_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

| 31 | 30 | 29 | 28 | ... | 0 |
|-----|-----|-----|-----|-----|---|
|     |     |     |     |     | Reset |

HP_APM_M1_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```