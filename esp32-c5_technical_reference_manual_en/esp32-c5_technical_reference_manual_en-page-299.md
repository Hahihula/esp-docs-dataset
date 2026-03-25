

```markdown
Register 7.42. EFUSE_INT_RAW_REG (0x01DC)

EFUSE_READ_DONE_INT_RAW  The raw interrupt status of EFUSE_READ_DONE_INT. (R/SS/WTC)
EFUSE_PGM_DONE_INT_RAW  The raw interrupt status of EFUSE_PGM_DONE_INT. (R/SS/WTC)


Register 7.43. EFUSE_INT_ST_REG (0x01E0)

EFUSE_READ_DONE_INT_ST  The masked interrupt status of EFUSE_READ_DONE_INT. (RO)
EFUSE_PGM_DONE_INT_ST  The masked interrupt status of EFUSE_PGM_DONE_INT. (RO)


Register 7.44. EFUSE_INT_ENA_REG (0x01E4)

EFUSE_READ_DONE_INT_ENA  Write 1 to enable EFUSE_READ_DONE_INT. (R/W)
EFUSE_PGM_DONE_INT_ENA  Write 1 to enable EFUSE_PGM_DONE_INT. (R/W)
```