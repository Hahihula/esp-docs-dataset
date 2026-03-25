

```markdown
Register 11.62. PMU_POWER_PD_HPCPU_CNTL_REG (0x0100)
```

Continued from the previous page...

PMU_FORCE_HP_CPU_NO_RESET Configures whether or not to forcefully prevent the reset of CPU domain. This setting has a lower priority than PMU_FORCE_HP_CPU_RESET.
- O: No effect
- 1: Force not reset
(R/W)

PMU_FORCE_HP_CPU_NO_ISO Configures whether or not to disable the force isolation of CPU domain. This setting has a lower priority than PMU_FORCE_HP_CPU_ISO.
- O: No effect
- 1: Disable
(R/W)

PMU_FORCE_HP_CPU_PD Configures whether or not to force power down CPU domain. This setting has a lower priority than PMU_FORCE_HP_CPU_PU.
- O: No effect
- 1: Force power down
(R/W)

PMU_PD_HP_CPU_MASK Configures whether or not to force power up CPU domain, regardless the signals from PMU.
- O: no effect
- 1: Force power up
(R/W)

PMU_PD_HP_CPU_PD_MASK Configures whether or not to force power down CPU domain, regardless the signals from PMU. This setting has a lower priority than PMU_PD_HP_CPU_MASK.
- O: No effect
- 1: Force power up
(R/W)
```