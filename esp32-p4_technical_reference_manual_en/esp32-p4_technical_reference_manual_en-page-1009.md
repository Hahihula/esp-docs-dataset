

```markdown
Register 14.9. PMU_HP_ACTIVE_HP_REGULATORO_REG (0x0028)

PMU_HP_ACTIVE_HP_REGULATOR_DBIAS Indicates the current voltage of the HP system regulator. (RO)
PMU_DIG_DBIAS_SEL Configures which of the following regulates the HP system regulator voltage.
  0: Regulated by Hardware automatically
  1: Regulated by Software
(R/W)

PMU_DIG_DBIAS_INIT Initializes the PVT voltage configurations. (WT)

PMU_HP_ACTIVE_HP_REGULATOR_XPD Configures whether to enable the HP sys regulator in HP_ACTIVE state.
  0: Disable the HP sys regulator
  1: Enable the HP sys regulator
(R/W)

PMU_HP_ACTIVE_REGULATOR_VO1_XPD Configures whether to enable VO1 regulator in HP_ACTIVE state.
  0: Disable
  1: Enable
(R/W)

PMU_HP_ACTIVE_HP_REGULATOR_DBIAS Regulates the voltage of the HP sys regulator in HP_ACTIVE state. The higher the value, the higher the voltage. (R/W)
```