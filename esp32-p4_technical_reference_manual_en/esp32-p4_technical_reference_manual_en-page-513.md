

```markdown
Register 8.8. EFUSE_RD_REPEAT_DATA4_REG (0x0040)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | EFUSE_DIS_SWD | EFUSE_DIS_WDT | EFUSE_DCDC_VSET_EN | EFUSE_HP_PWR_SRC_SEL | (reserved) | EFUSE_OPXA_TIEH_SEL_3 | EFUSE_OPXA_TIEH_SEL_2 | EFUSE_OPXA_TIEH_SEL_1 | EFUSE_OPXA_TIEH_SEL_0 | Reset |
|     | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 |    |

EFUSE_OPXA_TIEH_SEL_0 Represents what controls the power supply for LDO VOO.
- 0: The power supply is always high
  - 1: Controlled by the SDMMC1 peripheral
  - 2: Controlled by the PMU_LDO_VO_TIEH_0 register field
  - 3: Controlled by the SDMMCO peripheral (RO)

EFUSE_OPXA_TIEH_SEL_1 Represents what controls the power supply for LDO VO1.
- 0: Controlled by the PMU_LDO_VO_TIEH_1 register field
- 1: Controlled by the SDMMCO peripheral
- 2: The power supply is always high
- 3: Controlled by the SDMMC1 peripheral (RO)

EFUSE_OPXA_TIEH_SEL_2 Represents what controls the power supply for LDO VO2.
- 0: Controlled by the PMU_LDO_VO_TIEH_2 register field
- 1: Controlled by the SDMMCO peripheral
- 2: The power supply is always high
- 3: Controlled by the SDMMC1 peripheral (RO)

EFUSE_OPXA_TIEH_SEL_3 Represents what controls the power supply for LDO VO3.
- 0: Controlled by the PMU_LDO_VO_TIEH_3 register field
- 1: Controlled by the SDMMCO peripheral
- 2: The power supply is always high
- 3: Controlled by the SDMMC1 peripheral (RO)

Continued on the next page...
```