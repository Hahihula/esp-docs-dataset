

```markdown
Register 60.28. LP_ANA_TOUCH_PADn_THO_REG (n: 1-14) (0x0150+0xC*(n-1))

LP_ANA_TOUCH_PADn_THO

31 | 16 | 15 | ... | 0
-----------------------------------------------
0x00 | 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset

LP_ANA_TOUCH_PADn_THO Configures the touch threshold for touch sensor n for sampling frequency mode 0. (R/W)

Register 60.29. LP_ANA_TOUCH_PADn_TH1_REG (n: 1-14) (0x0154+0xC*(n-1))

LP_ANA_TOUCH_PADn_TH1

31 | 16 | 15 | ... | 0
-----------------------------------------------
0x00 | 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset

LP_ANA_TOUCH_PADn_TH1 Configures the touch threshold of touch sensor n for sampling frequency mode 1. (R/W)

Register 60.30. LP_ANA_TOUCH_PADn_TH2_REG (n: 1-14) (0x0158+0xC*(n-1))

LP_ANA_TOUCH_PADn_TH2

31 | 16 | 15 | ... | 0
-----------------------------------------------
0x00 | 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset

LP_ANA_TOUCH_PADn_TH2 Configures the touch threshold of touch sensor n for sampling frequency mode 2. (R/W)
```