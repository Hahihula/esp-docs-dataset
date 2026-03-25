

```markdown
Register 11.46. PMU_LP_SLEEP_XTAL_REG (0x00BC)

PMU_LP_SLEEP_XPD_XTAL   Configures whether to enable XTAL_CLK in LP_SLEEP state.
    0: Disable
    1: Enable
    (R/W)
```

```markdown
Register 11.47. PMU_LP_SLEEP_LP_DIG_POWER_REG (0x00C0)

PMU_LP_SLEEP_LP_MEM_DSLP   Configures whether to enable Memory Deep-sleep mode for the 320 KB SRAM in LP_SLEEP state.
    0: Disable
    1: Enable
    (R/W)
```

```markdown
PMU_LP_SLEEP_PD_LP_PERI_PD_EN   Configures whether to power down the "Peripherals+ROM" domain in LP_SLEEP state.
    0: Power up
    1: Power down
    (R/W)
```