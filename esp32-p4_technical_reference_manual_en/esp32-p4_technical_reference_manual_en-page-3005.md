

```markdown
Register 60.22. LP_ANA_TOUCH_CLR_REG (0x0124)

LP_ANA_TOUCH_CHANNEL_CLR Write 1 to independently clear the touch state of the 14 touch sensors. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid. (WT)

LP_ANA_TOUCH_STATUS_CLR Write 1 to clear the touch state. (WT)


Register 60.23. LP_ANA_TOUCH_APPROACH_REG (0x0128)

LP_ANA_TOUCH_APPROACH_PAD0 Configure the first touch pin used in proximity mode. Configurable values are 1-14. Other values are invalid. (R/W)

LP_ANA_TOUCH_APPROACH_PAD1 Configure the second touch pin used in proximity mode. Configurable values are 1-14. Other values are invalid. (R/W)

LP_ANA_TOUCH_APPROACH_PAD2 Configure the third touch pin used in proximity mode. Configurable values are 1-14. Other values are invalid. (R/W)

LP_ANA_TOUCH_SLP_APPROACH_EN Configures whether to enable proximity mode.
0: Disable
1: Enable
(R/W)
```