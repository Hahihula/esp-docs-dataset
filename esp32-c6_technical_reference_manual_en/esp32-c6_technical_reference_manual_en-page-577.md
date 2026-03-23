

```markdown
## Register 16.12. HP_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

| Bit 31 | Bit 23 | Bit 22 | Bit 18 | Bit 17 | Bit 16 | Bit 15 |
|--------|--------|--------|--------|--------|--------|--------|
|   O    |   O    |   O    |   HP_APM_M1_EXCEPTION_ID |        |        |        |
| (reserved) |        |        |        |        |        |        |

HP_APM_M1_EXCEPTION_REGION  Represents exception region. (RO)
HP_APM_M1_EXCEPTION_MODE     Represents exception mode. (RO)
HP_APM_M1_EXCEPTION_ID       Represents exception id information. (RO)

## Register 16.13. HP_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

| Bit 31 |        |
|--------|--------|
|   O    | Reset |

HP_APM_M1_EXCEPTION_ADDR     Represents exception addr. (RO)

## Register 16.14. HP_APM_M2_STATUS_REG (0x00E8)

| Bit 31 | ... | Bit 2 | Bit 1 | Bit 0 |
|--------|-----|-------|-------|-------|
|   O    |     |       | Reset |       |

HP_APM_M2_EXCEPTION_STATUS  Represents exception status.
bit0: 1 represents authority_exception
bit1: 1 represents space_exception
(RO)
```