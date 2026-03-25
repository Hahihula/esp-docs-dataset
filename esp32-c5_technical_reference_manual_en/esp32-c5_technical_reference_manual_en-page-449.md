

```markdown
## Register 9.77. PCR_TIMERGROUP_XTAL_CONF_REG (0x0160)

PCR_TGO_XTAL_RST_EN Configures whether to reset the clock calibration function of the Timer Group O.
- 0: Not reset
- 1: Reset
(R/W)

PCR_TGO_XTAL_CLK_EN Configures whether to enable the clock calibration function of the Timer Group O.
- 0: Not enable
- 1: Enable
(R/W)
```

```markdown
## Register 9.78. PCR_KM_CONF_REG (0x0164)

PCR_KM_CLK_EN Configures whether to enable the clock of the Key Manager.
- 0: Not enable
- 1: Enable
(R/W)

PCR_KM_RST_EN Configures whether to reset the Key Manager.
- 0: Not reset
- 1: Reset
(R/W)

PCR_KM_READY Represents whether or not the Key Manager is released from reset.
- 0: Not released
- 1: Released
(RO)
```