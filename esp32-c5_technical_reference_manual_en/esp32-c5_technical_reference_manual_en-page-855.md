

```markdown
Chapter 21 Power Supply Detector GoBack

Register 21.1. LP_ANA_BOD_MODEO_CNTL_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LP_ANA_BOD_MODEO_RESET_ENA                                                 |
| 30  | LP_ANA_BOD_MODEO_RESET_SEL                                                 |
| 29  | LP_ANA_BOD_MODEO_INTR_ENA                                                  |
| 28  | LP_ANA_BOD_MODEO_CNTL_CLR                                                  |
| 18  | LP_ANA_BOD_MODEO_RESET_WAIT                                                |
| 17  | LP_ANA_BOD_MODEO_PD_RF_ENA                                                 |
| 8   | LP_ANA_BOD_MODEO_INTR_WAIT                                                 |
| 7   | (reserved)                                                                  |
| 6   | LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA                                           |
| 5   | LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA                                           |
| 0   | Reset                                                                       |

LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA Configures whether to enable the brown-out detector to trigger flash suspend.
    0: Disable
    1: Enable
    (R/W)

LP_ANA_BOD_MODEO_PD_RF_ENA Configures whether to enable the brown-out detector to power down the RF module.
    0: Disable
    1: Enable
    (R/W)

LP_ANA_BOD_MODEO_INTR_WAIT Configures the time to generate an interrupt after the brown-out signal is valid. The unit is LP_FAST_CLK cycles. (R/W)

LP_ANA_BOD_MODEO_RESET_WAIT Configures the time to generate a reset after the brown-out signal is valid. The unit is LP_FAST_CLK cycles. (R/W)

LP_ANA_BOD_MODEO_CNTL_CLR Configures whether to clear the count value of the brown-out detector.
    0: Do not clear
    1: Clear
    (R/W)

LP_ANA_BOD_MODEO_INTR_ENA Enables the interrupts for the brown-out detector mode 0. LP_ANA_BOD_MODEO_INT_RAW and LP_ANA_BOD_MODEO_LP_INT_RAW are valid only when this field is set to 1.
    0: Disable
    1: Enable
    (R/W)

LP_ANA_BOD_MODEO_RESET_SEL Configures the reset type when the brown-out detector is triggered.
    0: Chip reset
    1: System reset
    (R/W)
```
Continued on the next page...
```