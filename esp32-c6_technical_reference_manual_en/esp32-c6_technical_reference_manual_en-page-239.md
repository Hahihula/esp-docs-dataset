

```markdown
Register 6.107. EFUSE_INT_RAW_REG (0x01D8)

EFUSE_READ_DONE_INT_RAW The raw interrupt status of read_done. (R/SS/WTC)
EFUSE_PGM_DONE_INT_RAW The raw interrupt status of pgm_done. (R/SS/WTC)

Register 6.108. EFUSE_INT_ST_REG (0x01DC)

EFUSE_READ_DONE_INT_ST The masked interrupt status of read_done. (RO)
EFUSE_PGM_DONE_INT_ST The masked interrupt status of pgm_done. (RO)

Register 6.109. EFUSE_INT_ENA_REG (0x01EO)

EFUSE_READ_DONE_INT_ENA Write 1 to enable read_done interrupt. (R/W)
EFUSE_PGM_DONE_INT_ENA Write 1 to enable pgm_done interrupt. (R/W)
```