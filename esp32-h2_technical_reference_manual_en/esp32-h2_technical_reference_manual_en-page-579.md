

```markdown
|Bit|31|30|29|28|27|18|17|8|7|6|5|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|Value|0| | | | | | | | | | |Reset|

LP_ANA_BOD_MODEO_CLOSE_FLASH_ENA Configures whether to enable the brown-out detector to trigger flash suspend.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_PD_RF_ENA Configures whether to enable the brown-out detector to power down the RF module.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_INTR_WAIT Configures the time to generate an interrupt after the brown-out signal is valid. The unit is LP_FAST_CLK cycles. (R/W)

LP_ANA_BOD_MODEO_RESET_WAIT Configures the time to generate a reset after the brown-out signal is valid. The unit is LP_FAST_CLK cycles. (R/W)

LP_ANA_BOD_MODEO_CNT_CLR Configures whether to clear the count value of the brown-out detector.
- O: Do not clear
- 1: Clear
(R/W)

LP_ANA_BOD_MODEO_INTR_ENA Enables the interrupts for the brown-out detector mode 0. LP_ANA_BOD_MODEO_INT_RAW are valid only when this field is set to 1.
- O: Disable
- 1: Enable
(R/W)

LP_ANA_BOD_MODEO_RESET_SEL Configures the reset type when the brown-out detector is triggered.
- O: Chip reset
- 1: System reset
(R/W)
```