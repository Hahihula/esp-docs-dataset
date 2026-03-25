

```markdown
Register 11.80. PMU_HP_CK_CNTL_REG (0x0150)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 16  | PMU_SWITCH_ICG_CNTL_WAIT       | Configures the number of wait cycles required after switching the Integrated Clock Gating (ICG) module to its modified configuration, ensuring the transition is properly completed. (R/W) |
| 8   | PMU_MODIFY_ICG_CNTL_WAIT       | Configures the number of wait cycles required after modifying the input configurations of the Integrated Clock Gating (ICG) module, ensuring the changes take effect and the clock signals stabilize. (R/W) |

Register 11.81. PMU_RF_PWC_REG (0x0158)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 29  | PMU_XPD_PLL_I2C                 | Configures the PLL clock generation. (R/W)                                  |
| 28  | PMU_XPD_CKGEN_I2C               | Configures the 5G clock generation. (R/W)                                   |
| 27  | PMU_XPD_RFRX_PBUS              | Configures the RF receiving output. (R/W)                                   |
| 26  | PMU_XPD_TXRF_I2C                | Configures the RF transmitting output. (R/W)                                |
| 25  | PMU_XPD_PERIF_I2C_RSTB         | Configures the I2C reset. (R/W)                                            |
| 24  | PMU_XPD_RX5G_I2C                | Configures the 5G receiving output. (R/W)                                   |
| 23  | PMU_XPD_TC5G_I2C                | Configures the 5G transmitting output. (R/W)                                |
| 22-0|                                 | Reset                                                                       |
```