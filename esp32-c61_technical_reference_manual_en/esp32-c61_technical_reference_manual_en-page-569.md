

```markdown
Register 11.61. PMU_POWER_PD_HPAON_CNTL_REG (0x00FC)

Continued from the previous page...

PMU_PD_HP_AON_MASK Configures whether or not to force power up Modem Power domain, regardless the signals from PMU.
O: No effect
1: Force power up
(R/W)

PMU_PD_HP_AON_PD_MASK Configures whether or not to force power down Modem Power domain, regardless the signals from PMU. This setting has a lower priority than PMU_PD_HP_AON_MASK.
O: No effect
1: Force power up
(R/W)

Register 11.62. PMU_POWER_PD_HPCPU_CNTL_REG (0x0100)
```

```markdown
PMU_FORCE_HP_CPU_RESET Configures whether or not to force reset CPU domain.
O: No effect
1: Force reset
(R/W)

PMU_FORCE_HP_CPU_ISO Configures whether or not to enable the force isolation of CPU domain.
O: No effect
1: Enable
(R/W)

PMU_FORCE_HP_CPU_PU Configures whether or not to force power up CPU domain. This setting has a lower priority than PMU_PD_HP_CPU_MASK.
O: No effect
1: Force power up
(R/W)
```

```markdown
Continued on the next page...
```