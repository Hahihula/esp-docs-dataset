

```markdown
Register 14.42. PMU_RF_PWC_REG (0x015C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | ... | 0 |
|-----|----|----|----|----|----|----|----|----|----|-----|---|
|     |    |    |    | (reserved) | PMU_XPD_PERIF_I2C_RSTB PDO | PMU_SDIO_PLL_XPD | PMU_MSPI_PHY_XPD | ... | Reset |

PMU_MSPI_PHY_XPD  Configures whether to enable MSPI PHY.
0: Disable
1: Enable
(R/W)

PMU_SDIO_PLL_XPD  Configures whether to enable SDIO PLL.
0: Disable
1: Enable
(R/W)

PMU_PERIF_I2C_RSTB  Configures whether to enable reset for PERI I2C.
0: Reset
1: Release
(R/W)

PMU_XPD_PERIF_I2C  Configures whether to enable the power for PERI ADC.
0: Disable
1: Enable
(R/W)
```