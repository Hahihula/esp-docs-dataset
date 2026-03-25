

```markdown
Register 11.63. PMU_POWER_PD_HPWFIFI_CNTL_REG (0x0108)

| 31 | 27 | 26 |        11         | 10 |   6   | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|-------------------|----|-------|---|---|---|---|---|---|
|    | O  | O  | O O O O O O O O O | O  |       |   |   |   |   |   | Reset |

PMU_FORCE_HP_WIFI_RESET Configures whether or not to force reset MODEM domain.
0: No effect
1: Force reset
(R/W)

PMU_FORCE_HP_WIFI_ISO Configures whether or not to enable the force isolation of MODEM domain.
0: No effect
1: Enable
(R/W)

PMU_FORCE_HP_WIFI_PU Configures whether or not to force power up MODEM domain. This setting has a lower priority than PMU_PD_HP_WIFI_MASK.
0: No effect
1: Force power up
(R/W)

PMU_FORCE_HP_WIFI_NO_RESET Configures whether or not to forcefully prevent the reset of MODEM domain. This setting has a lower priority than PMU_FORCE_HP_WIFI_RESET.
0: No effect
1: Force not reset
(R/W)

PMU_FORCE_HP_WIFI_NO_ISO Configures whether or not to disable the force isolation of MODEM domain. This setting has a lower priority than PMU_FORCE_HP_WIFI_ISO.
0: No effect
1: Disable
(R/W)

PMU_FORCE_HP_WIFI_PD Configures whether or not to force power down MODEM domain. This setting has a lower priority than PMU_FORCE_HP_WIFI_PU.
0: No effect
1: Force power down
(R/W)
```