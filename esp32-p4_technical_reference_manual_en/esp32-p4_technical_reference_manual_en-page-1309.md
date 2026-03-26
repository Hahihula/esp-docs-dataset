

```markdown
Register 20.B3. HP_SYSTEM_ICM_SLV_ARB_PRIORITY_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    | (reserved) | HP_SYSTEM_ICM_L2MEM_PRIORITY | HP_SYSTEM_ICM_FLASH_MSPI_PRIORITY | HP_SYSTEM_ICM_PSRAM_MSPI_PRIORITY | HP_SYSTEM_ICM_LCD_PRIORITY | HP_SYSTEM_ICM_CAM_PRIORITY | (reserved) | Reset |

HP_SYSTEM_ICM_L2MEM_PRIORITY Configures the arbitration priority of L2MEM for response channels among slaves connected to SYS ICM. (R/W)

HP_SYSTEM_ICM_FLASH_MSPI_PRIORITY Configures the arbitration priority of FLASH MSPI for response channels among slaves connected to SYS ICM. (R/W)

HP_SYSTEM_ICM_PSRAM_MSPI_PRIORITY Configures the arbitration priority of PSRAM MSPI for response channels among slaves connected to SYS ICM. (R/W)

HP_SYSTEM_ICM_LCD_PRIORITY Configures the arbitration priority of MIPI_LCD registers for response channels among slaves connected to SYS ICM. (R/W)

HP_SYSTEM_ICM_CAM_PRIORITY Configures the arbitration priority of MIPI_CAM registers for response channels among slaves connected to SYS ICM. (R/W)
```