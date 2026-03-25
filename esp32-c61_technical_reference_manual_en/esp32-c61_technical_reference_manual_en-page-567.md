

```markdown
Chapter 11 Low-Power Management

Register 11.60. PMU_POWER_PD_TOP_CNTL_REG (0x00F8)

Continued from the previous page...

PMU_PD_TOP_MASK Configures whether or not to force power up "Peripherals+ROM" domain, regardless the signals from PMU.
O: No effect
1: Force power up
(R/W)

PMU_PD_TOP_PD_MASK Configures whether or not to force power down "Peripherals+ROM" domain, regardless the signals from PMU. This setting has a lower priority than PMU_PD_TOP_MASK.
O: No effect
1: Force power up
(R/W)
```