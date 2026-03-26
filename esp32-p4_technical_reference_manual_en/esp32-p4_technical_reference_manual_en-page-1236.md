

```markdown
Register 19.87. PMS_HP_COREn_UM_PMS_REGO_REG (n: 0-1) (0x000C+0x8*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 30  | PMS_HP_COREn_UM_LP_TRNG_ALLOW | Configures whether HP CPU in user mode has permission to access LP TRNG.     |
| 29  | PMS_HP_COREn_UM_LP_SRAM_ALLOW | Configures whether HP CPU in user mode has permission to access LP SRAM.     |
| 28  | PMS_HP_COREn_UM_LP_TSENS_ALLOW| Configures whether HP CPU in user mode has permission to access LP TSENS.    |
| 27  | PMS_HP_COREn_UM_LP_P2P_ALLOW   | Configures whether HP CPU in user mode has permission to access LP P2P.      |
| 26  | PMS_HP_COREn_UM_LP_EFUSE_ALLOW | Configures whether HP CPU in user mode has permission to access LP EFUSE.    |
| 25  | PMS_HP_COREn_UM_LP_INTR_ALLOW  | Configures whether HP CPU in user mode has permission to access LP INTR.     |
| 24  | PMS_HP_COREn_UM_LP_IOMUX_ALLOW | Configures whether HP CPU in user mode has permission to access LP IOMUX.    |
| 23  | PMS_HP_COREn_UM_LP_TOUCH_ALLOW | Configures whether HP CPU in user mode has permission to access LP TOUCH.    |
| 22  | PMS_HP_COREn_UM_LP_ADC_ALLOW   | Configures whether HP CPU in user mode has permission to access LP ADC.      |
| 21  | PMS_HP_COREn_UM_LP_I2C0_ALLOW  | Configures whether HP CPU in user mode has permission to access LP I2C0.     |
| 20  | PMS_HP_COREn_UM_LP_I2C1_ALLOW  | Configures whether HP CPU in user mode has permission to access LP I2C1.     |
| 19  | PMS_HP_COREn_UM_LP_SPI_ALLOW   | Configures whether HP CPU in user mode has permission to access LP SPI.      |
| 18  | PMS_HP_COREn_UM_LP_UART_ALLOW  | Configures whether HP CPU in user mode has permission to access LP UART.     |
| 17  | PMS_HP_COREn_UM_LP_PERI0X8T_ALLOW | Configures whether HP CPU in user mode has permission to access LP PERI0x8T.|
| 16  | PMS_HP_COREn_UM_LP_MAILBOX_ALLOW| Configures whether HP CPU in user mode has permission to access LP MAILBOX.  |
| 15  | PMS_HP_COREn_UM_LP_WDT_ALLOW   | Configures whether HP CPU in user mode has permission to access LP WDT.      |
| 14  | PMS_HP_COREn_UM_LP_PMU_ALLOW   | Configures whether HP CPU in user mode has permission to access LP PMU.      |
| 13  | PMS_HP_COREn_UM_LP_ANAPERI_ALLOW| Configures whether HP CPU in user mode has permission to access LP ANAPERI.  |
| 12  | PMS_HP_COREn_UM_LP_SYSGREG_ALLOW| Configures whether HP CPU in user mode has permission to access LP SYSGREG.  |
| 11  | (reserved)                    |                                                                             |
| 10  | (reserved)                    |                                                                             |
| 9   | (reserved)                    |                                                                             |
| 8   | (reserved)                    |                                                                             |
| 7   | (reserved)                    |                                                                             |
| 6   | (reserved)                    |                                                                             |
| 5   | (reserved)                    |                                                                             |
| 4   | (reserved)                    |                                                                             |
| 3   | (reserved)                    |                                                                             |
| 2   | (reserved)                    |                                                                             |
| 1   | (reserved)                    |                                                                             |
| 0   | Reset                         |                                                                             |

PMS_HP_COREn_UM_LP_SYSGREG_ALLOW Configures whether HP CPU in user mode has permission to access LP System Registers.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_UM_LP_AONCLKRST_ALLOW Configures whether HP CPU in user mode has permission to access LP_AONCLKRST.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_UM_LP_TIMER_ALLOW Configures whether HP CPU in user mode has permission to access LP timer.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_UM_LP_ANAPERI_ALLOW Configures whether HP CPU in user mode has permission to access LP ANAPERI.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_UM_LP_PMU_ALLOW Configures whether HP CPU in user mode has permission to access LP PMU.
O: Not allowed
1: Allowed
(R/W)

Continued on the next page...
```