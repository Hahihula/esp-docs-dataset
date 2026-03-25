

```markdown
Register 7.69. PCR_CTRL_32K_CONF_REG (0x0130)

PCR_32K_SEL Configures the 32 kHz clock for TIMER_GROUP.
O: Invalid. No effect
1: XTAL32K_CLK
2/3: OSC_SLOW_CLK
(R/W)
```

```markdown
Register 7.70. PCR_SRAM_POWER_CONF_O_REG (0x0134)

PCR_ROM_FORCE_PU Configures whether or not to force power up ROM.
O: Not force power up
1: Force power up
(R/W)

PCR_ROM_FORCE_PD Configures whether or not to force power down ROM.
O: Not force power down
1: Force power down
(R/W)

PCR_ROM_CLKGATE_FORCE_ON Configures whether to force enable clocks and bypass clock gating when accessing ROM.
O: Use clock gating
1: Force enable clocks and bypass clock gating
(R/W)
```