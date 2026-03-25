

```markdown
Chapter 11 Low-Power Management

Register 11.63. PMU_POWER_PD_HPWIFI_CNTL_REG (0x0108)

Continued from the previous page...

PMU_PD_HP_WIFI_MASK    Configures whether or not to force power up MODEM domain, regardless the signals from PMU.
                        O: No effect
                        1: Force power up
                        (R/W)

PMU_PD_HP_WIFI_PD_MASK Configures whether or not to force power down MODEM domain, regardless the signals from PMU. This setting has a lower priority than PMU_PD_HP_WIFI_MASK.
                        O: No effect
                        1: Force power up
                        (R/W)
```