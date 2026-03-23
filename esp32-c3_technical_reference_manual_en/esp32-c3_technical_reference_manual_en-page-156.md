

```markdown
Register 4.110. EFUSE_STATUS_REG (0x01D0)

EFUSE_STATE Indicates the state of the eFuse state machine. (RO)
EFUSE_REPEAT_ERR_CNT Indicates the number of error bits during programming BLOCK0. (RO)


Register 4.111. EFUSE_INT_RAW_REG (0x01D8)

EFUSE_READ_DONE_INT_RAW The raw bit signal for read_done interrupt. (R/WC/SS)
EFUSE_PGM_DONE_INT_RAW The raw bit signal for pgm_done interrupt. (R/WC/SS)


Register 4.112. EFUSE_INT_ST_REG (0x01DC)

EFUSE_READ_DONE_INT_ST The status signal for read_done interrupt. (RO)
EFUSE_PGM_DONE_INT_ST The status signal for pgm_done interrupt. (RO)
```