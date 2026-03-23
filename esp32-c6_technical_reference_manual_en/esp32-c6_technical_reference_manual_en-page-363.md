

```markdown
Register 8.71. PCR_SRAM_POWER_CONF_REG (0x0138)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                       |                                                                             |
| 21  | PCR_ROM_CLKGATE_FORCE_ON       | Configures whether or not to force open the clock and bypass the gate-clock when accessing the ROM. <br> O: A gate-clock will be used when accessing the ROM. <br> 1: Force to open the clock and bypass the gate-clock when accessing the ROM. (R/W) |
| 20  | PCR_ROM_FORCE_PD               | Configures whether or not to force power down ROM. <br> O: Not force power down <br> 1: Force power down (R/W) |
| 18  | PCR_ROM_FORCE_PU               | Configures whether or not to force power up ROM. <br> O: Not force power up <br> 1: Force power up (R/W) |
| 17  | PCR_SRAM_CLKGATE_FORCE_ON      | Configures whether or not to force open the clock and bypass the gate-clock when accessing the SRAM. <br> O: A gate-clock will be used when accessing the SRAM. <br> 1: Force to open the clock and bypass the gate-clock when accessing the SRAM. (R/W) |
| 15  | PCR_SRAM_FORCE_PD              | Configures whether or not to force power down SRAM. <br> O: Not force power down <br> 1: Force power down (R/W) |
| 14  | PCR_SRAM_FORCE_PU              | Configures whether or not to force power up SRAM. <br> O: Not force power up <br> 1: Force power up (R/W) |
```