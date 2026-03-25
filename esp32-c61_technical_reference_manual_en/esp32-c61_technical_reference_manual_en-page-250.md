

```markdown
Chapter 5 eFuse Controller (EFUSE)

Register 5.41. EFUSE_INT_RAW_REG (0x01D8)
```
| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31:2| reserved                       |                                                                             |
| 1   | EFUSE_PGM_DONE_INT_RAW         | Represents the raw interrupt status of pgm_done. (R/SS/WTC)                  |
| 0   | EFUSE_READ_DONE_INT_RAW        | Represents the raw interrupt status of read_done. (R/SS/WTC)                 |

Register 5.42. EFUSE_INT_ST_REG (0x01DC)
```
| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31:2| reserved                       |                                                                             |
| 1   | EFUSE_PGM_DONE_INT_ST          | Represents the masked interrupt status of pgm_done. (RO)                     |
| 0   | EFUSE_READ_DONE_INT_ST         | Represents the masked interrupt status of read_done. (RO)                    |

Register 5.43. EFUSE_INT_ENA_REG (0x01EO)
```
| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31:2| reserved                       |                                                                             |
| 1   | EFUSE_PGM_DONE_INT_ENA         | Write 1 to enable pgm_done interrupt. (R/W)                                 |
| 0   | EFUSE_READ_DONE_INT_ENA        | Write 1 to enable read_done interrupt. (R/W)                                |

Espressif Systems
250
ESP32-C61 TRM (Pre-release v0.5)
PRELIMINARY

Submit Documentation Feedback
```