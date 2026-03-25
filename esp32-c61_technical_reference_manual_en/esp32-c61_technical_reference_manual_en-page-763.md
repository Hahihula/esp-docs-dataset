

```markdown
Chapter 19 Power Supply Detector

Register 19.1. LP_ANA_BOD_MODEO_CNTL_REG (0x0000)

Continued from the previous page...

LP_ANA_BOD_MODEO_RESET_ENA Configures whether to enable reset for the brown-out detector.
O: Disable
1: Enable
(R/W)

Register 19.2. LP_ANA_BOD_MODE1_CNTL_REG (0x0004)

LP_ANA_BOD_MODE1_RESET_ENA Configures whether to enable brown-out detector mode 1.
O: Disable
1: Enable
(R/W)

Register 19.3. LP_ANA_POWER_GLITCH_CNTL_REG (0x0008)

LP_ANA_PWR_GLITCH_RESET_ENA Configures whether to enable the voltage glitch detectors.
Bit0, bit1, bit2, bit3 correspond to VDDPST2/3, VDDPST1, VDDA3, and VDDA8, respectively.
O: Disable
1: Enable
(R/W)
```