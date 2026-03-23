

```markdown
Register 12.80. LP_ANA_BOD_MODEO_CNTL_REG (0x0000)

| Bits | Description                                                                 |
|------|-----------------------------------------------------------------------------|
| 31   | LP_ANA_BOD_MODEO_RESET_ENA                                                 |
| 30   | LP_ANA_BOD_MODEO_RESET_SEL                                                 |
| 29   | LP_ANA_BOD_MODEO_INTR_ENA                                                  |
| 28   | LP_ANA_BOD_MODEO_CNT_CLR                                                   |
| 18   | LP_ANA_BOD_MODEO_RESET_WAIT                                                |
| 17   | LP_ANA_BOD_MODEO_PD_RF_ENA                                                 |
| 6    | LP_ANA_BOD_MODEO_INTR_WAIT                                                 |
| 5    | (reserved)                                                                  |
| 0    | LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA                                           |

```

LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA Configures whether to enable the brownout detector to trigger flash suspend.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_PD_RF_ENA Configures whether to enable the brownout detector to close the RF module.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_INTR_WAIT Configures the time to generate an interrupt after the brownout signal is valid. The unit is LP_FAST_CLK. (R/W)

LP_ANA_BOD_MODEO_RESET_WAIT Configures the time to generate a reset after the brownout signal is valid. The unit is LP_FAST_CLK. (R/W)

LP_ANA_BOD_MODEO_CNT_CLR Configures whether to clear the count value of the brownout detector.
- O: Do not clear
- 1: Clear
(R/W)

LP_ANA_BOD_MODEO_INTR_ENA Enables the interrupts for the brownout detector mode 0. LP_ANA_BOD_MODEO_INT_RAW and LP_ANA_BOD_MODEO_LP_INT_RAW are valid only when this field is set to 1. (R/W)

LP_ANA_BOD_MODEO_RESET_SEL Configures the reset type when the brownout detector is triggered.
- O: Chip reset
- 1: System reset
(R/W)

LP_ANA_BOD_MODEO_RESET_ENA Configures whether to enable reset for the brownout detector.
- O: Disable
- 1: Enable
(R/W)
```