

```markdown
Register 11.34. PMU_RF_PWC_REG (0x0154)

PMU_XPD_PERIF_I2C Configures whether to power up the SAR ADC.
O: Do not power up
1: Power up
(R/W)
```

```markdown
Register 11.35. PMU_VDDBAT_CFG_REG (0x0158)

PMU_VDDBAT_MODE Represents the source status of VDD_RTC. (RO)
PMU_VDDBAT_SW_UPDATE Software drives the VBAT controller to update the source of VDD_RTC.
(WT)
```

```markdown
Register 11.36. PMU_INT_RAW_REG (0x0160)

PMU_SOC_SLEEP_REJECT_INT_RAW The raw interrupt status of PMU_SOC_SLEEP_REJECT_INT.
(R/WTC/SS)
PMU_SOC_WAKEUP_INT_RAW The raw interrupt status of PMU_SOC_WAKEUP_INT. (R/WTC/SS)
```