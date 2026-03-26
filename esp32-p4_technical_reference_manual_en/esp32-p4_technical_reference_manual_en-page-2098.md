

```markdown
## Register 40.36. CSI_HOST_INT_ST_ERR_ECC_CORRECTED_REG (0x02D0)

| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  |                                                                             |
| ... |                                                                             |
| 1   | Reset                                                                       |

**CSI_HOST_ST_ERR_ECC_CORRECTED_VCn (n: 0-15)** Represents whether the ERR_ECC_CORRECTED_VCn error occurs.
- 0: Do not occur
- 1: Occur (RC)
```

```markdown
## Register 40.37. CSI_HOST_INT_MSK_ERR_ECC_CORRECTED_REG (0x02D4)

| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  |                                                                             |
| ... |                                                                             |
| 1   | Reset                                                                       |

**CSI_HOST_MASK_ERR_ECC_CORRECTED_VCn (n: 0-15)** Configures whether to mask CSI_HOST_ST_ERR_ECC_CORRECTED_VCn.
- 0: Mask the error interrupt
- 1: Enable the error interrupt (R/W)
```

Espressif Systems 2098  
Submit Documentation Feedback ESP32-P4 TRM PRELIMINARY
```