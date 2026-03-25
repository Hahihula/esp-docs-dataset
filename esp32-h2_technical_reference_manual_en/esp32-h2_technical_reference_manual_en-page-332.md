

```markdown
## Register 7.71. PCR_SRAM_POWER_CONF_1_REG (0x0138)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| 30  | PCR_SRAM_CLKGATE_FORCE_ON   | Configures whether to force enable clocks and bypass clock gating when accessing SRAM.<br>0: Use clock gating<br>1: Force enable clocks and bypass clock gating (R/W) |
| 29  | reserved                    |                                                                             |
| 25  | PCR_SRAM_FORCE_PD           | Configures whether or not to force power down SRAM.<br>0: Not force power down<br>1: Force power down (R/W) |
| 24  | reserved                    |                                                                             |
| 15  | PCR_SRAM_FORCE_PU           | Configures whether or not to force power up SRAM.<br>0: Not force power up<br>1: Force power up (R/W) |
| 14  | reserved                    |                                                                             |
| 10  | PCR_SRAM_FORCE_PD           | Same as above                                                                |
| 9   | reserved                    |                                                                             |
| 5   | PCR_SRAM_FORCE_PU           | Same as above                                                                |
| 4   | reserved                    |                                                                             |
| 0   | Reset                       | 0x1F                                                                          |

### Field Descriptions

- **PCR_SRAM_FORCE_PU**: Configures whether or not to force power up SRAM.
  - 0: Not force power up
  - 1: Force power up (R/W)

- **PCR_SRAM_FORCE_PD**: Configures whether or not to force power down SRAM.
  - 0: Not force power down
  - 1: Force power down (R/W)

- **PCR_SRAM_CLKGATE_FORCE_ON**: Configures whether to force enable clocks and bypass clock gating when accessing SRAM.
  - 0: Use clock gating
  - 1: Force enable clocks and bypass clock gating (R/W)
```

```markdown
## Register 7.72. PCR_SEC_CONF_REG (0x013C)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| ... | ...                         |                                                                             |
| 2   | PCR_SEC_CLK_SEL             | Configures the clock source for the External Memory Encryption and Decryption module.<br>0 (default): XTAL_CLK<br>1: RC_FAST_CLK<br>2: PLL_F64M_CLK<br>3: PLL_F96M_CLK (R/W) |
| 1   | reserved                    |                                                                             |
| 0   | Reset                       | 0                                                                              |

### Field Descriptions

- **PCR_SEC_CLK_SEL**: Configures the clock source for the External Memory Encryption and Decryption module.
  - 0 (default): XTAL_CLK
  - 1: RC_FAST_CLK
  - 2: PLL_F64M_CLK
  - 3: PLL_F96M_CLK (R/W)
```