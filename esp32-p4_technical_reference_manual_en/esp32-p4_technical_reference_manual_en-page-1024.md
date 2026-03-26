

```markdown
Register 14.26. PMU_LP_SLEEP_LP_DIG_POWER_REG (0x00C0)

PMU_LP_SLEEP_PD_LP_PERI_PD_EN   Configures whether to enable LP GPIO function in LP_SLEEP state.
    O: Disable
    1: Enable
        (R/W)

PMU_LP_SLEEP_BOD_SOURCE_SEL   Configures whether to enable brown-out detection in LP_SLEEP state. (R/W)

PMU_LP_SLEEP_VDBAT_MODE   Configures whether to enable VBAT power in LP_SLEEP state.
    O: Disable
    1: Enable
        (R/W)

PMU_LP_SLEEP_LP_MEM_DSLP   Configures whether to enable Memory Deep-sleep mode for the LP SRAM in LP_SLEEP state.
    O: Disable
    1: Enable
        (R/W)

PMU_LP_SLEEP_PD_LP_PERI_PD_EN   Configures whether to power down LP PD Peripherals in LP_SLEEP state.
    O: Power up
    1: Power down
        (R/W)
```