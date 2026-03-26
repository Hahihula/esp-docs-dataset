

```markdown
Register 20.34. HP_SYSTEM_L2_MEM_INT_RECORD1_REG (0x00B4)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-26     | (reserved)                                 |                                                                             |
| 25        | HP_SYSTEM_L2_CACHE_ERR_BANK                | Records the bank number of L2 cache ECC error. (RO)                          |
| 17-14     | HP_SYSTEM_L2_MEM_ECC_ERR_BIT               | Records the flipped bit that triggered L2_MEM_ECC_ERR_INT. (RO)              |
| 13        | (reserved)                                 |                                                                             |
| 0         | HP_SYSTEM_L2_MEM_ECC_ERR_INT_ADDR          | Records the address when L2_MEM_ECC_ERR_INT occurs. (RO)                     |

HP_SYSTEM_L2_MEM_ECC_ERR_INT_ADDR Records the address when L2_MEM_ECC_ERR_INT occurs. (RO)

HP_SYSTEM_L2_MEM_ECC_ONE_BIT_ERR Records the error when L2_MEM_ECC_ERR_INT occurs. (RO)

HP_SYSTEM_L2_MEM_ECC_ERR_BIT Records the flipped bit that triggered L2_MEM_ECC_ERR_INT. (RO)

HP_SYSTEM_L2_CACHE_ERR_BANK Records the bank number of L2 cache ECC error. (RO)
```

```markdown
Register 20.35. HP_SYSTEM_L2_MEM_L2_CACHE_ECC_REG (0x00C4)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-1      | (reserved)                                 |                                                                             |
| 0         | HP_SYSTEM_L2_CACHE_ECC_EN                  | Configures whether or not to enable the ECC check for L2 cache.            |
|           |                                             | 0: Disable                                                                   |
|           |                                             | 1: Enable                                                                    |
|           |                                             | (R/W)                                                                        |

HP_SYSTEM_L2_CACHE_ECC_EN Configures whether or not to enable the ECC check for L2 cache.
```

```markdown
GoBack

Chapter 20 System Registers (SYSREG)

Espressif Systems

Submit Documentation Feedback

ESP32-P4 TRM
PRELIMINARY

1277
```